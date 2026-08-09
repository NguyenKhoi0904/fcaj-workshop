---
title: "Week 4 Worklog"
date: 2026-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---


### Week 4 Objectives:
* Learn about Database Concepts, Amazon RDS, Amazon Aurora, Amazon Redshift, and Amazon ElastiCache.
* Gain hands-on experience with AWS CloudWatch and granting applications access to AWS resources using IAM Roles.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Learn about:<br>&emsp;+ What is a Database? <br>&emsp;+ Core database concepts <br>&emsp;+ Relational databases and non-relational databases <br>&emsp;+ What is OLTP (Online Transaction Processing)? <br>&emsp;+ What is OLAP (Online Analytical Processing)? <br> -**Hands-on:**<br>&emsp;+ Create an EC2 Instance <br>&emsp;+ Create an S3 Bucket <br>&emsp;+ Create an IAM User and Access Key <br>&emsp;+ Connect to the EC2 Instance <br>&emsp;+ Use an Access Key to upload files to S3 <br>&emsp;+ Create an IAM Role <br>&emsp;+ Use an IAM Role to upload files to S3                                               |  13/07/2026  |  13/07/2026  | <https://www.youtube.com/watch?v=OOD2RwWuLRw&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=217><br><https://000048.awsstudygroup.com/vi/> |
| 3   | - Learn about:<br>&emsp;+ Amazon RDS (Relational Database Service) <br>&emsp;+ Amazon Aurora <br>&emsp;+ What is Amazon Redshift? <br>&emsp;+ What is Amazon ElastiCache?                                              |  14/07/2026  |  14/07/2026  | <https://www.youtube.com/watch?v=qbrobQZrokY&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=218><br><https://www.youtube.com/watch?v=UvdiRW34aNI&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=219> |
| 4   | - **Hands-on:**<br>&emsp;+ Deploy a CloudFormation Stack <br>&emsp;+ View Metrics <br>&emsp;+ Perform searches <br>&emsp;+ Perform mathematical operations <br>&emsp;+ Create dynamic labels <br>&emsp;+ Create CloudWatch Logs <br>&emsp;+ Create CloudWatch Logs Insights queries <br>&emsp;+ Create CloudWatch Metric Filters <br>&emsp;+ Configure CloudWatch Alarms <br>&emsp;+ Create CloudWatch Dashboards                                              |  15/07/2026  |  15/07/2026  | <https://000008.awsstudygroup.com/vi/> |
| 5   | - **Hands-on:**<br>&emsp;+ Create a VPC <br>&emsp;+ Create an EC2 Security Group <br>&emsp;+ Create an RDS Security Group <br>&emsp;+ Create a DB Subnet Group <br>&emsp;+ Create an EC2 Instance <br>&emsp;+ Create an RDS Database Instance <br>&emsp;+ Deploy an application <br>&emsp;+ Perform backup and restore operations                                              |  16/07/2026  |  16/07/2026  | <https://000005.awsstudygroup.com/vi/> |
| 6   | - Practice using SageMaker Studio by following the lab, but encountered errors related to Service Quotas <br> - Investigate and resolve issues related to Service Quotas, including Total Domains = 0, Maximum Studio User Profiles = 0, and Maximum Running Studio Apps = 0                                              |  17/07/2026  |  17/07/2026  | https://cloudjourney.awsstudygroup.com/vi/7-aimlservice/ |


### Results Achieved in Week 4:
* Understand the fundamental concepts of databases, including:
  * Core concepts of database management systems.
  * Differences between relational databases and non-relational (NoSQL)   databases.
  * Online Transaction Processing (OLTP).
  * Online Analytical Processing (OLAP).
* Understand the functions and use cases of AWS database services, including:
  * Amazon RDS.
  * Amazon Aurora.
  * Amazon Redshift.
  * Amazon ElastiCache.
* Gain hands-on experience managing access to AWS resources through:
  * IAM Users and Access Keys.
  * IAM Roles.
  * Accessing Amazon S3 from EC2 using Access Keys and IAM Roles.
* Understand the advantages of using IAM Roles over Access Keys when granting permissions to AWS resources.
* Gain hands-on experience using AWS CloudFormation to deploy infrastructure following the Infrastructure as Code (IaC) approach.
* Gain hands-on experience monitoring and tracking systems using Amazon CloudWatch, including:
  * Monitoring Metrics.
  * Analyzing CloudWatch Logs and Logs Insights.
  * Creating Metric Filters.
  * Configuring CloudWatch Alarms.
  * Building CloudWatch Dashboards.
* Gain hands-on experience deploying applications using Amazon RDS, including:
  * Creating a VPC and Security Group.
  * Creating a DB Subnet Group.
  * Launching an EC2 Instance and an RDS Database Instance.
  * Connecting an application to the database.
  * Performing data backup and restoration.
* Become familiar with Amazon SageMaker Studio and understand AWS Service Quotas management mechanisms.
* Identify and analyze the causes of Service Quotas-related errors in SageMaker Studio, such as:
  * Total Domains.
  * Maximum Studio User Profiles.
  * Maximum Running Studio Apps.