<details>
<summary>Kinesis Data Firehose</summary>
<br>
Amazon Kinesis Data Firehose is the easiest way to reliably load streaming data into data lakes, data stores, and analytics tools. It can capture, transform, and load streaming data into Amazon S3, Amazon Redshift, Amazon Elasticsearch Service, and Splunk, enabling near real-time analytics with existing business intelligence tools and dashboards you’re already using today. It is a fully managed service that automatically scales to match the throughput of your data and requires no ongoing administration.
</details>

<details>
<summary>Amazon EMR</summary>
<br>
Amazon EMR is the industry-leading cloud big data platform for processing vast amounts of data using open source tools such as Apache Spark, Apache Hive, Apache HBase, Apache Flink, Apache Hudi, and Presto. With EMR you can run Petabyte-scale analysis at less than half of the cost of traditional on-premises solutions and over 3x faster than standard Apache Spark. Amazon EMR uses Hadoop, an open-source framework, to distribute your data and processing across a resizable cluster of Amazon EC2 instances.
<br>
Additionally, you can use Amazon EMR to transform and move large amounts of data into and out of other AWS data stores and databases such as Amazon Simple Storage Service (Amazon S3) and Amazon DynamoDB.

</details>

<details>
<summary>ASG</summary>
<br>
 <b>cooldown period</b>
 - It ensures that the Auto Scaling group does not launch or terminate additional EC2 instances before the previous scaling activity takes effect.
 - Its default value is 300 seconds.
 
 
 
 <details>
 <summary>(ASG) is not terminating an unhealthy Amazon EC2 instance</summary>
 <br>
  The health check grace period for the instance has not expired <br>
  The instance maybe in Impaired status - Amazon EC2 Auto Scaling does not immediately terminate instances with an Impaired status.<br>
  The instance has failed the ELB health check status - By default, Amazon EC2 Auto Scaling doesn't use the results of ELB health checks to determine an instance's health status when the group's health check configuration is set to EC2.<br>
<br>You are billed for instances as soon as they are launched, including the time that they are not yet in service.
<br>
 </details>
</details>

<details>
<summary>RDS</summary>
<br>
RDS db instance, running as a multi-AZ deployment - performs synchronous data replication
<br>
RDS custom (for Oracle) - you can customize your database and OS - access instance (ssh/ssm) 
<br>
<b>Aurora native function</b>
You can invoke an AWS Lambda function from an Amazon Aurora MySQL-Compatible Edition DB cluster with a native function or a stored procedure. This approach can be useful when you want to integrate your database running on Aurora MySQL with other AWS services. For example, you might want to capture data changes whenever a row in a table is modified in your database.
<br>
Q:  ensure that the database can automatically failover to an RDS instance to continue operating in the event of failure. The architecture should also be as highly available as possible.
<br>
You can run an Amazon RDS DB instance in several AZs with Multi-AZ deployment. Amazon automatically provisions and maintains a secondary standby DB instance in a different AZ. Your primary DB instance is synchronously replicated across AZs to the secondary instance to provide data redundancy, failover support, eliminate I/O freezes, and minimize latency spikes during systems backup.

</details>

<details>
<summary>DynamoDB</summary>
<br>
Q: You have to design a solution to detect new entries in the DynamoDB table then automatically trigger a Lambda function to run some tests to verify the processed data.
<br>
enabling DynamoDB Streams to capture table activity and automatically trigger the Lambda function
</details>


<details>
<summary>Rekognition</summary>
makes it easy to add image and video analysis to your applications <br>
you can identify objects, people, text, scenes, and activities in images and videos, as well as detect any inappropriate content. Amazon Rekognition also provides highly accurate facial analysis and facial search capabilities that you can use to detect, analyze, and compare faces for a wide variety of user verification, people counting
<br>
</details>
<details>
<summary>Guardduty</summary>
 <a href='https://aws.amazon.com/guardduty/'>https://aws.amazon.com/guardduty/</a><br>
Amazon GuardDuty is a threat detection service that continuously monitors your AWS accounts and workloads for malicious activity and delivers detailed
<br>
Amazon GuardDuty offers threat detection that enables you to continuously monitor and protect your AWS accounts, workloads, and data stored in Amazon S3. GuardDuty analyzes continuous streams of meta-data generated from your account and network activity found in AWS CloudTrail Events, Amazon VPC Flow Logs, and DNS Logs.
</details>

<details>
<summary>Macie</summary>
Macie is a data security service that uses machine learning (ML) and pattern matching to discover and help protect your sensitive data.
<br>
</details>

<details>
<summary>Inspector</summary>
 <a href='https://aws.amazon.com/inspector/'>https://aws.amazon.com/inspector/</a><br>
Amazon Inspector is an automated vulnerability management service that continually scans AWS workloads for software vulnerabilities and unintended network exposure.
<br>
 Amazon Inspector security assessments help you check for unintended network accessibility of your Amazon EC2 instances and for vulnerabilities on those EC2 instances. Amazon Inspector assessments are offered to you as pre-defined rules packages mapped to common security best practices and vulnerability definitions.
</details>

<details>
<summary>Amazon Comprehend</summary>
<br>
is a natural language processing (NLP) service that uses machine learning to find meaning and insights in text.
<br>
You can use Amazon Comprehend to determine the sentiment of a document. For example, you can use sentiment analysis to determine the sentiments of comments on a blog posting or a transcribed call to determine if your users loved or hated your content. You can determine sentiment for documents in any of the primary languages supported by Amazon Comprehend. All documents in one job must be in the same language.
</details>

<details>
<summary>Cognito</summary>
<br>
 Cognito is just a service for user authentication and authorization
</details>

<details>
<summary>AWS Backup </summary>
<br>
 is a centralized backup service that makes it easy and cost-effective for you to backup your application data across AWS services in the AWS
<br>
WS Backup makes protecting your AWS storage volumes, databases, and file systems simple by providing a central place where you can configure and audit the AWS resources you want to backup, automate backup scheduling, set retention policies, and monitor all recent backup and restore activity.
<br>A company needs to use Amazon Aurora as the Amazon RDS database engine of their web application. The Solutions Architect has been instructed to implement a 90-day backup retention policy
</details>

<details>
<summary>AWS License Manager</summary>
<br>
is a service that makes it easier for you to manage your software licenses from software vendors (for example, Microsoft, SAP, Oracle, and IBM) centrally across AWS and your on-premises environments. 
</details>

<details>
<summary>Lambda</summary>
<br>
Lambda@Edge is a feature of Amazon CloudFront that lets you run code closer to users of your application, which improves performance and reduces latency. With Lambda@Edge, you don't have to provision or manage infrastructure in multiple locations around the world. You pay only for the compute time you consume 
</details>

<details>
<summary>S3</summary>
<br>
lifecycle policies 
<br>
Objects must be stored for at least 30 days in the current storage class before you can transition them to <b>STANDARD_IA or ONEZONE_IA</b>
<br>
This limitation does not apply to <b>INTELLIGENT_TIERING, GLACIER, and DEEP_ARCHIVE</b> storage class
<br>
 <b>Glacier Select</b> is incorrect because this is not a storage service. It is primarily used to run queries directly on data stored in Amazon Glacier, retrieving only the data you need out of your archives to use for analytics.
 
 <br><br>
When you configure your bucket as a static website, the website is available at the AWS Region-specific website endpoint of the bucket.
Depending on your Region, your Amazon S3 website endpoints follow one of these two formats.
 
- s3-website dash (-) Region ‐ http://bucket-name.s3-website.Region.amazonaws.com
- s3-website dot (.) Region ‐ http://bucket-name.s3-website-Region.amazonaws.com
 
 <br>
<b>Amazon S3 access points</b> simplify data access for any AWS service or customer application that stores data in S3. Access points are named network endpoints that are attached to buckets that you can use to perform S3 object operations, such as GetObject and PutObject.<br>
You can configure any access point to accept requests only from a virtual private cloud (VPC) to restrict Amazon S3 data access to a private network. You can also configure custom block public access settings for each access point.
 <br><br>
 Amazon S3 Transfer Acceleration can speed up content transfers to and from Amazon S3 by as much as 50-500% for long-distance transfer of larger objects. 
<br><br>
<hr>
questions:
<br>
How can Amazon S3 invoke actions based on file activity within a bucket?
- Amazon S3 Event Notifications
<br>
<b>CORS Configure the cross-origin resource sharing</b> will only allow objects from one domain (travel.cebu.com) to be loaded and accessible to a different domain (palawan.com). 

</details>



<details>
<summary>AWS Glue</summary>
<br>
It is a fully managed extract, transform, and load (ETL) service that makes it easy for customers to prepare and load their data for analytics.
</details>

<details>
<summary>Network Access Analyzer</summary>
<br>
Network Access Analyzer is a feature of VPC that reports on unintended access to your AWS resources based on the security and compliance that you set.
<br>This service is not capable of performing deep packet inspection on traffic entering or leaving your VPC, unlike AWS Network Firewall.
</details>

<details>
<summary>AWS Network Firewall</summary>
<br>
AWS Network Firewall is a stateful, managed, network firewall, and intrusion detection and prevention service for your virtual private cloud (VPC). 
<br>With Network Firewall, you can filter traffic at the perimeter of your VPC. This includes traffic going to and coming from an internet gateway, NAT gateway, or over VPN or AWS Direct Connect.
<br>
You can use Network Firewall to monitor and protect your Amazon VPC traffic in a number of ways, including the following:

- Pass traffic through only from known AWS service domains or IP address endpoints, such as Amazon S3.
- Use custom lists of known bad domains to limit the types of domain names that your applications can access.
- Perform deep packet inspection on traffic entering or leaving your VPC.
- Use stateful protocol detection to filter protocols like HTTPS, independent of the port used.
</details>

<details>
<summary>AWS Transit Gateway</summary>
<br>
With AWS Transit Gateway, you can simplify the connectivity between multiple VPCs and also connect to any VPC attached to AWS Transit Gateway with a single VPN connection.<br>
AWS Transit Gateway also enables you to scale the IPsec VPN throughput with equal-cost multi-path (ECMP) routing support over multiple VPN tunnels. A single VPN tunnel still has a maximum throughput of 1.25 Gbps. If you establish multiple VPN tunnels to an ECMP-enabled transit gateway, it can scale beyond the default limit of 1.25 Gbps.

![alt text](folder1/transitGW.png)
</details>

<details>
<summary>AWS AppSync</summary>
<br>
AWS AppSync is a serverless GraphQL and Pub/Sub API service that simplifies building modern web and mobile applications. It provides a robust, scalable GraphQL interface for application developers to combine data from multiple sources, including Amazon DynamoDB, AWS Lambda, and HTTP APIs.
</details>

<details>
<summary>AWS CloudTrail</summary>
<br>
CloudTrail is primarily used to monitor and record the account activity across your AWS resources and not your web applications. You cannot use CloudTrail to capture the detailed information of all HTTP requests that go through your public-facing Application Load Balancer (ALB). CloudTrail can only track the resource changes made to your ALB, but not the actual IP traffic that goes through it.
</details>

<details>
<summary>CloudWatch Container Insights</summary>
<br>
 The primary function of CloudWatch Container Insights is to collect, aggregate, and summarize metrics and logs from your containerized applications and microservices.
</details>

<details>
<summary>Amazon CloudWatch Application Insights</summary>
<br>
Amazon CloudWatch Application Insights facilitates observability for your applications and underlying AWS resources. It helps you set up the best monitors for your application resources to continuously analyze data for signs of problems with your applications. Application Insights, which is powered by SageMaker and other AWS technologies, provides automated dashboards that show potential problems with monitored applications, which help you to quickly isolate ongoing issues with your applications and infrastructure. 
</details>

<details>
<summary>Amazon FSx </summary>
<br>
Amazon FSx is a fully managed third-party file system solution. It uses SSD storage to provide fast performance with low latency.
<details>
<summary>Amazon FSx for Lustre</summary>
<br>
Amazon FSx for Lustre provides a high-performance file system optimized for fast processing of workloads such as machine learning, high performance computing (HPC), video processing, financial modeling, and electronic design automation (EDA). These workloads commonly require data to be presented via a fast and scalable file system interface and typically have data sets stored on long-term data stores like Amazon S3.
<br>
With Amazon FSx, you can launch and run a file system that provides sub-millisecond access to your data and allows you to read and write data at speeds of up to hundreds of gigabytes per second of throughput and millions of IOPS.
<br>
</details>

<details>
<summary>Amazon FSx for Windows File Server</summary>
<br>
</details>
A fully managed native Microsoft Windows file system with full support for the SMB protocol, Windows NTFS, and Microsoft Active Directory (AD) integration.

</details>

<details>
<summary>Amazon Lex</summary>
<br>
 A service that can help you build conversational interfaces using voice and text.
 <br>
 Amazon Lex enables you to build applications using a speech or text interface powered by the same technology that powers Amazon Alexa. Amazon Lex provides the deep functionality and flexibility of natural language understanding (NLU) and automatic speech recognition (ASR), so you can build highly engaging user experiences with lifelike conversational interactions and create new categories of products.
</details>

<details>
<summary>ElastiCache</summary>
<br>
<details>
<summary>ElastiCache for Redis</summary>
<br>
Redis, which stands for Remote Dictionary Server, is a fast, open-source, in-memory key-value data store for use as a database, cache, message broker, and queue. Redis now delivers sub-millisecond response times enabling millions of requests per second for real-time applications in Gaming, Ad-Tech, Financial Services, Healthcare, and IoT. Redis is a popular choice for caching, session management, gaming, leaderboards, real-time analytics, geospatial, ride-hailing, chat/messaging, media streaming, and pub/sub apps.
</details>

<details>
<summary>ElastiCache for Memcached</summary>
<br>
Memcached, a high-performance distributed memory cache service, is designed for simplicity while Redis offers a rich set of features that make it effective for a wide range of use cases. Memcached does not offer support for geospatial data.
only one feature Memcached is better then Redis - it has multithreaded architecture
</details>
</details>

<hr>
<h2><b>security</b></h2>
<br>
<details>
<summary> Service Control Policies</summary>
<br>
An AWS Organization is using Service Control Policies (SCP) for central control over the maximum available permissions for all accounts in their organization. 
<br>

- SCPs do not affect service-linked role
- If user or role has an IAM permission policy that grants access to an action that is either not allowed or explicitly denied by the applicable SCPs, the user or role can't perform that action 
 - SCPs affect all users and roles in attached accounts, including the root user
</details>

<hr>

<h2><b>NETWORK</b></h2>
<br>
<details>
<summary> VPC</summary>
<br>
An AWS Organization is using Service Control Policies (SCP) for central control over the maximum available permissions for all accounts in their organization. 
<br>

When using VPC Endpoints, what are the only two AWS services that have a Gateway Endpoint available?
- Amazon S3 and DynamoDB These two services have a VPC Gateway Endpoint (remember it), all the other ones have an Interface endpoint (powered by Private Link - means a private IP).

- <b>Gateway endpoint</b> is a type of VPC endpoint that provides reliable connectivity to Amazon S3 and DynamoDB without requiring an internet gateway or a NAT device for your VPC. Instances in your VPC do not require public IP addresses to communicate with resources in the service.
<br>When you create a Gateway endpoint, you can attach an <b>endpoint policy<b/> that controls access to the service to which you are connecting. You can modify the endpoint policy attached to your endpoint and add or remove the route tables used by the endpoint. An endpoint policy does not override or replace IAM user policies or service-specific policies (such as S3 bucket policies). It is a separate policy for controlling access from the endpoint to the specified service.


</details>

<details>
<summary>AWS Global Accelerator</summary>
<br>

AWS Global Accelerator is a network layer service that directs traffic to optimal endpoints over the AWS global network, this improves the availability and performance of your internet applications. It provides two static anycast IP addresses that act as a fixed entry point to your application endpoints in a single or multiple AWS Regions, such as your Application Load Balancers, Network Load Balancers, Elastic IP addresses or Amazon EC2 instances, in a single or in multiple AWS regions.
<br>
AWS Global Accelerator uses endpoint weights to determine the proportion of traffic that is directed to endpoints in an endpoint group, and traffic dials to control the percentage of traffic that is directed to an endpoint group (an AWS region where your application is deployed).
<br>
With AWS Global Accelerator, you can shift traffic gradually or all at once between the blue and the green environment and vice-versa without being subject to DNS caching on client devices and internet resolvers, traffic dials and endpoint weights changes are effective within seconds.
<br>
WS Global Accelerator always routes user traffic to the optimal endpoint based on performance, reacting instantly to changes in application health, your user’s location, and policies that you configure. Global Accelerator is a good fit for non-HTTP use cases, such as gaming (UDP), IoT (MQTT), or Voice over IP. 
</details>

<details>
<summary>Route 53</summary>
<br>
You can use Route 53 to perform three main functions in any combination: domain registration, DNS routing, and health checking.

- Geoproximity Routing - route traffic to your resources based on the geographic location of your users and your resources.
- Geolocation Routing - lets you choose the resources that serve your traffic based on the geographic location of your users, meaning the location that DNS queries originate from.
</details>
<hr>


<details>
<summary>AWS Control Tower</summary>
<br>
AWS Control Tower simply offers the easiest way to set up and govern a new, secure, multi-account AWS environment. This is not the most suitable service to use to securely share your resources across AWS accounts or within your Organization. You have to use AWS Resources Access Manager (RAM) instead.
<br>
</details>

<details>
<summary>AWS Resource Access Manager (RAM)</summary>
<br>
is a service that enables you to easily and securely share AWS resources with any AWS account or within your AWS Organization. You can share AWS Transit Gateways, Subnets, AWS License Manager configurations, and Amazon Route 53 Resolver rules resources with RAM.
</details>

<details>
<summary> Amazon SQS</summary>
<br>
you can configure the message retention period to a value from 1 minute to 14 days. The default is 4 days. Once the message retention limit is reached, your messages are automatically deleted.
<br>
 A single Amazon SQS message queue can contain an unlimited number of messages. However, there is a 120,000 limit for the number of inflight messages for a standard queue and 20,000 for a FIFO queue. Messages are inflight after they have been received from the queue by a consuming component, but have not yet been deleted from the queue.
<br>
</details>

 <details>
<summary>simple</summary>
<br>
</details>
