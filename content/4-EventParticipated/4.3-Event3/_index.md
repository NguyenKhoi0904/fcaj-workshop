---
title: "Event 3"
date: 2026-01-01
weight: 1
chapter: false
pre: " <b> 4.2. </b> "
---

# Summary Report: “Agent Forge - Deepdive Day 2”

**Time:** 9:00 AM - 12:00 PM, Saturday, 08/08/2026  
**Location:** 26th Floor, Bitexco Financial Tower, 2 Hai Trieu Street, Saigon, Ho Chi Minh City 700000, Vietnam.  
**Role:** Attendee  
**Speakers:** <br>
- Nghia Tran - Agentic SA
- Anh Pham - Cloud Consultant, G-AsiaPacific Vietnam

##### Main Content:
The theoretical session covered the following main topics:
- **Memory**
    - Memory helps Agents retain information, overcome context window limitations, and personalize user experiences.
    - Short-term Memory: stores raw data from conversations and synchronizes it for fast retrieval of the most recent information.
    - Long-term Memory: extracts insights and knowledge from conversations, converts them into vectors, and stores them for long-term use.
    - Memory Strategies: include Summary, User Preference, Semantic, and Episodic.
    - Namespace: organizes data in a hierarchical structure such as /Strategy/Actor/Session, helping narrow the search scope, reduce token usage, and improve retrieval speed.
- **Evaluations**
    - Evaluations ensure that Agents operate accurately, usefully, and safely, while detecting hallucinations, reasoning errors, and inappropriate tool selection.
    - There are two modes:
        - On-demand Evaluation: proactive evaluation during development.
        - Online Evaluation: continuous monitoring in production through telemetry and metrics.
    - Evaluations are performed at three levels:
        - Session level: evaluates the entire session.
        - Trace level: evaluates individual responses.
        - Span level: evaluates tool usage and parameters.
    - The system uses a Judge to analyze Agent activities and then sends the results to Observability so SMEs can monitor and intervene.
- **Observability**
    - Observability helps developers understand, debug, and optimize the internal operation of Agents.
    - Three main components:
        - Logs: show what happened.
        - Traces: show how it happened.
        - Metrics: measure impacts such as latency, token cost, and error rate.
    - It also includes OpenTelemetry, real-time monitoring, alerts, and a hierarchical data structure from Session → Trace → Span/Sub-span.
- **AgentCore Components**
    - The main components include:
        - **Registry:** a central hub for managing and reusing Agent skills, tools, and APIs; supports Admin, Publisher, and Consumer roles.
        - **Harness:** a minimal framework for initializing an Agent from a Model + System Prompt + Tool, while also supporting extensibility.
        - **Tools:** enable Agents to interact with external systems, perform actions, and access real-time data/APIs.
        - **Payments:** enables Agents to make payments; currently supports Stripe and Coinbase.
        - **Optimization:** uses data from Evaluation and Observability to identify areas for improvement, supporting A/B testing, Red Teaming, and self-optimizing loops.
        - **Policy:** a control layer for Agent behavior, security, and compliance; supports Human-in-the-loop, Cedar, Strict/Permissive modes, and the Least Privilege principle.

The hands-on session provided technical guidance on deployment using the Agent SDK, setting up AWS Bedrock, and using command-line tools (CLI) to create a project, deploy, and test an Agent on AWS.

#### Key Takeaways
Through the Agent Forge - Deepdive Day 2 event, I gained a deeper understanding of the components required to build and operate an AI Agent in a production environment, particularly the roles of Memory, Evaluations, and Observability in maintaining context, evaluating quality, and monitoring Agent activities. I also learned how AgentCore components such as Registry, Harness, Tools, Policy, and Optimization work together to manage, scale, secure, and continuously improve Agents. In particular, I recognized the importance of Least Privilege and Human-in-the-loop in controlling Agent actions. Finally, the hands-on session helped me become familiar with the Agent SDK, AWS Bedrock, and AWS CLI, while also providing an understanding of the basic workflow from project initialization and deployment to Agent testing on AWS.

#### Some Photos from the Event
<img src="/fcaj-workshop/images/AWS_Event_3_01.jpg" alt="My profile" width="50%">
