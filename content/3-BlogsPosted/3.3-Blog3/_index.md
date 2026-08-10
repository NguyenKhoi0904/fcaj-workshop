---
title: "Blog 3"
date: 2026-01-01
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---

# From Theory to Implementation: Data Engineering Challenges in a Real-World GenAI/RAG Project

Hello everyone,

In my previous article, I shared my perspective on what a Data Engineer should prioritize when learning AWS to optimize learning time and prepare for real-world work.

Today, I would like to share more about how I applied those AWS concepts and AWS services directly to my practical project. Although the main problem of the project belongs to the **GenAI / RAG (Retrieval-Augmented Generation)** domain, when I started implementing the system architecture, I realized: **Up to 80% of the system's strength and stability lies in the Data Engineering layer**.

Below is an overview of how I applied cloud data processing techniques to this project.

Dưới đây là bức tranh toàn cảnh về cách mình ứng dụng các kỹ thuật xử lý dữ liệu cloud trong đồ án này.
## 1. Data Ingestion & Event-Driven Pipeline (Data Ingestion Flow)
When processing input documents, if we simply follow the traditional approach of directly calling a processing function, the system can easily become a bottleneck or overloaded. Therefore, I designed the system based on an **Event-Driven Architecture**:

- **Automatic Triggering (S3 Event Trigger)**: Whenever a user or Admin uploads a new document (PDF/TXT/Scan) to Amazon S3 Raw Documents, an event (S3 Event) immediately triggers the processing flow without requiring manual polling.
- **Buffer Queue & System Decoupling (Amazon SQS)**: To prevent the system from becoming overwhelmed when a large number of files are uploaded simultaneously, I route the data through **Amazon S3 Event → Amazon SQS (Buffer Queue)**. Using SQS acts as a load-bearing buffer, combined with an automatic Retry mechanism and Dead Letter Queue (DLQ) to capture failed messages, ensuring zero data loss.
## 2. ETL & Unstructured Data Processing (Data Extraction & Transformation)
Unstructured text data needs to go through a rigorous ETL process before it can serve AI models:
- **Data Extraction (OCR)**: AWS Lambda receives messages from SQS and automatically calls Amazon Textract to perform OCR, accurately extracting text from scanned files or complex PDFs.
- **Structuring & Vector Storage (Chunking & Vectorization)**: After processing, the data is divided into smaller chunks using the **Parent-Child** approach, and then the Embedding API is called to transform them into vectors. All of this structural information is stored in **Amazon DynamoDB** – optimized for **Hybrid Search** queries (combining Cosine Similarity and BM25 using the RRF algorithm) to achieve the highest possible search accuracy.
## 3. Low-Latency Data Retrieval & Caching (Real-Time Query Optimization)
A core challenge in Data Engineering for Web/App applications is **latency** and **cost**:
- **Semantic Caching**: I integrated **Amazon ElastiCache Serverless** as an intelligent caching layer for queries. If a new question has semantics similar to a previous question, the system returns the result directly from the Cache instead of calling the expensive LLM again. This technique significantly reduces latency for end users (Real-time serving).
- **State & Response Management (Transaction Store)**: All conversation history (Chat History) and response data (Feedback Store) are stored in **DynamoDB** – a NoSQL Database that provides extremely fast write performance with latency measured in milliseconds.
## 4. Automated Batch Processing & Continuous Evaluation (Automated Evaluation Pipeline)
Beyond real-time data flows, a well-designed data system always needs a periodic processing flow (Batch Pipeline) to evaluate quality:
- **Automated Batch Job**: I use **Amazon EventBridge Scheduler** together with **AWS Lambda** to automatically launch the model quality evaluation pipeline (based on the RAGAS evaluation criteria) at a fixed time every day.
- **Periodic Data Lake Storage**: The daily evaluation results are pushed to **Amazon S3 Evaluation Results**, which serves as a Data Lake for storing historical logs. This allows the team to easily monitor and analyze trends in system quality over time.

## 5. Data Observability & Monitoring (Monitoring Data Flows)
Finally, data running in a Cloud system needs to be "visible" (observable) so that issues can be detected in a timely manner:
- **Centralized Logs & Metrics**: I use **Amazon CloudWatch** to collect logs and monitor important pipeline metrics such as: DLQ Depth, API Gateway 5xx error rate, and custom AI metrics such as Faithfulness, Relevancy, and Precision.
- **Intelligent Alert Routing**: Incidents are classified by severity level (Warning vs Critical). When a Critical error occurs, Amazon SNS works together with **AWS Chatbot** to immediately send alerts to **Slack** or **PagerDuty** for the technical team to handle.

## Three Data Engineering "Highlights" I Took Away from the Project
If you are also preparing to work on a project or personal project, here are the three Data Engineering principles that I found most valuable when applying them to this problem:
- **Decoupling:** The data ingestion and query serving layers operate independently through SQS and DynamoDB. Even if an Admin uploads thousands of PDF files simultaneously, the end-user chat experience remains completely smooth and unaffected.
- **Asynchronous Serverless Processing:** Combining S3 Event + SQS + Lambda allows the system to operate completely asynchronously. Computing resources are only activated when data passes through the system, helping optimize 100% of Cloud operating costs.
- **Query Optimization:** Instead of "naively" querying the LLM directly, combining Semantic Cache (ElastiCache) and Hybrid Search (BM25 + Vector Search) demonstrates the data performance optimization mindset of a Data Engineer.

## Conclusion
This project has helped me prove one thing: **Being a Data Engineer is not only about writing SQL statements or running Spark scripts, but also about the ability to design reliable Cloud infrastructure, automate data flows, and optimize the operating costs of a system**.

I hope this perspective from a practical project gives you a more vivid picture of how AWS services such as S3, SQS, Lambda, DynamoDB, and ElastiCache work together in Data Engineering.

## Link
<https://www.facebook.com/groups/awsstudygroupfcj/permalink/2240430060055287/?rdid=rnUr8B9OmLkzFWRU#>