---
layout: home
title: "professional cloud architect"
date: 2025-04-09 12:00:00 +0800
lastupdated: 2025-04-09 12:00:00 +0800
categories: cloud
tags: [ai,k8s,cloud]
---
professional cloud architect 2025-04-09 12:00:00

# 16
You have been asked to select the storage system for the click-data of your company's large portfolio of websites. This data is streamed in from a custom website analytics package at a typical rate of 6,000 clicks per minute. With bursts of up to 8,500 clicks per second. It must have been stored for future analysis by your data science and user experience teams.
Which storage infrastructure should you choose?  
您被要求选择用于存储贵公司大量网站点击数据的存储系统。这些数据以每分钟 6,000 次点击的典型速率从自定义网站分析包中流式传输。最高可达每秒 8,500 次点击。这些数据必须已存储以供您的数据科学和用户体验团队将来分析。
您应该选择哪种存储基础架构？
A. Google Cloud SQL  
B. Google Cloud Bigtable  
C. Google Cloud Storage  
D. Google Cloud Datastore  

Answer: B  
[Discussion](/assets/gcp/discussion/16.md)  


# 17
You are creating a solution to remove backup files older than 90 days from your backup Cloud Storage bucket. You want to optimize ongoing Cloud Storage spend.  
What should you do?
A. Write a lifecycle management rule in XML and push it to the bucket with gsutil  
B. Write a lifecycle management rule in JSON and push it to the bucket with gsutil  
C. Schedule a cron script using gsutil ls ג€"lr gs://backups/** to find and remove items older than 90 days  
D. Schedule a cron script using gsutil ls ג€"l gs://backups/** to find and remove items older than 90 days and schedule it with cron  

[Discussion](/assets/gcp/discussion/17.md)  


# 18
Your company is forecasting a sharp increase in the number and size of Apache Spark and Hadoop jobs being run on your local datacenter. You want to utilize the cloud to help you scale this upcoming demand with the least amount of operations work and code change.  
Which product should you use?  
您的公司预测，本地数据中心运行的 Apache Spark 和 Hadoop 作业的数量和规模将急剧增加。您希望利用云来帮助您以最少的操作工作和代码更改来扩展这一即将到来的需求。  
您应该使用哪种产品？
A. Google Cloud Dataflow  
B. Google Cloud Dataproc  
C. Google Compute Engine  
D. Google Kubernetes Engine  

[Discussion](/assets/gcp/discussion/18.md)  

# 19
The database administration team has asked you to help them improve the performance of their new database server running on Google Compute Engine. The database is for importing and normalizing their performance statistics and is built with MySQL running on Debian Linux. They have an n1-standard-8 virtual machine with 80 GB of SSD persistent disk.  
What should they change to get better performance from this system?  
数据库管理团队请您帮助他们提高在 Google Compute Engine 上运行的新数据库服务器的性能。该数据库用于导入和规范其性能统计数据，并使用在 Debian Linux 上运行的 MySQL 构建。他们有一个 n1-standard-8 虚拟机，带有 80 GB 的 SSD 永久磁盘。  
他们应该进行哪些更改才能从这个系统获得更好的性能？  
A. Increase the virtual machine's memory to 64 GB  
B. Create a new virtual machine running PostgreSQL  
C. Dynamically resize the SSD persistent disk to 500 GB  
D. Migrate their performance metrics warehouse to BigQuery  
E. Modify all of their batch jobs to use bulk inserts into the database  

[Discussion](/assets/gcp/discussion/19.md)  

# 20
You want to optimize the performance of an accurate, real-time, weather-charting application. The data comes from 50,000 sensors sending 10 readings a second, in the format of a timestamp and sensor reading.  
Where should you store the data?  
您想要优化一个精确、实时的天气图表应用程序的性能。数据来自 50,000 个传感器，它们每秒发送 10 个读数，格式为时间戳和传感器读数。  
您应该将数据存储在哪里？  
A. Google BigQuery  
B. Google Cloud SQL  
C. Google Cloud Bigtable  
D. Google Cloud Storage  

[Discussion](/assets/gcp/discussion/20.md)  


# 21
Your company's user-feedback portal comprises a standard LAMP stack replicated across two zones. It is deployed in the us-central1 region and uses autoscaled managed instance groups on all layers, except the database. Currently, only a small group of select customers have access to the portal. The portal meets a
99,99% availability SLA under these conditions. However next quarter, your company will be making the portal available to all users, including unauthenticated users. You need to develop a resiliency testing strategy to ensure the system maintains the SLA once they introduce additional user load.  
What should you do?  
贵公司的用户反馈门户包含一个跨两个区域复制的标准 LAMP 堆栈。它部署在 us-central1 区域，并在除数据库之外的所有层上使用自动扩展的托管实例组。目前，只有一小部分选定的客户可以访问该门户。  
在这些条件下，门户满足 99.99% 的可用性 SLA。但是下个季度，贵公司将向所有用户（包括未经身份验证的用户）提供该门户。您需要制定弹性测试策略，以确保系统在引入额外用户负载后保持 SLA。  
您应该怎么做？  

A. Capture existing users input, and replay captured user load until autoscale is triggered on all layers. At the same time, terminate all resources in one of the zones  
B. Create synthetic random user input, replay synthetic load until autoscale logic is triggered on at least one layer, and introduce ג€chaosג€ to the system by terminating random resources on both zones  
C. Expose the new system to a larger group of users, and increase group size each day until autoscale logic is triggered on all layers. At the same time, terminate random resources on both zones  
D. Capture existing users input, and replay captured user load until resource utilization crosses 80%. Also, derive estimated number of users based on existing user's usage of the app, and deploy enough resources to handle 200% of expected load  

[Discussion](/assets/gcp/discussion/21.md)  


# 22

One of the developers on your team deployed their application in Google Container Engine with the Dockerfile below. They report that their application deployments are taking too long.

You want to optimize this Dockerfile for faster deployment times without adversely affecting the app's functionality.  
Which two actions should you take? (Choose two.)  
您团队中的一位开发人员使用以下 Dockerfile 在 Google Container Engine 中部署了他们的应用程序。他们报告说他们的应用程序部署耗时太长。
FROM ubuntu:16.04  

COPY . /src  

RUN apt-get update && apt-get install -y python python-pip  

RUN pip install -r requirements.txt  
您想优化此 Dockerfile 以缩短部署时间，而不会对应用程序的功能产生不利影响。  
您应该采取哪两项措施？（选择两项。）  

A. Remove Python after running pip  
B. Remove dependencies from requirements.txt  
C. Use a slimmed-down base image like Alpine Linux  
D. Use larger machine types for your Google Container Engine node pools  
E. Copy the source after he package dependencies (Python and pip) are installed  

[Discussion](/assets/gcp/discussion/22.md)  


# 23
Your solution is producing performance bugs in production that you did not see in staging and test environments. You want to adjust your test and deployment procedures to avoid this problem in the future.  
What should you do?  
您的解决方案在生产中产生了性能错误，而您在暂存和测试环境中没有看到这些错误。您想调整测试和部署程序以避免将来出现此问题。  
您应该怎么做？  

A. Deploy fewer changes to production  
B. Deploy smaller changes to production  
C. Increase the load on your test and staging environments   
D. Deploy changes to a small subset of users before rolling out to production  

[Discussion](/assets/gcp/discussion/23.md)  


# 24
A small number of API requests to your microservices-based application take a very long time. You know that each request to the API can traverse many services.
You want to know which service takes the longest in those cases.  
What should you do?  
您的基于微服务的应用程序的少量 API 请求需要很长时间。您知道对 API 的每个请求都可以遍历许多服务。  
您想知道在这些情况下哪个服务花费的时间最长。  
您应该怎么做？  

A. Set timeouts on your application so that you can fail requests faster  
B. Send custom metrics for each of your requests to Stackdriver Monitoring  
C. Use Stackdriver Monitoring to look for insights that show when your API latencies are high  
D. Instrument your application with Stackdriver Trace in order to break down the request latencies at each microservice  

[Discussion](/assets/gcp/discussion/24.md)

# 25
During a high traffic portion of the day, one of your relational databases crashes, but the replica is never promoted to a master. You want to avoid this in the future.  
What should you do?  
在一天中的高流量时段，您的一个关系数据库崩溃了，但副本数据库从未升级为主数据库。您希望将来避免这种情况。
您应该怎么做？  

A. Use a different database  
B. Choose larger instances for your database  
C. Create snapshots of your database more regularly  
D. Implement routinely scheduled failovers of your databases

[Discussion](/assets/gcp/discussion/25.md)  

# 26
Your organization requires that metrics from all applications be retained for 5 years for future analysis in possible legal proceedings.
Which approach should you use?  
您的组织要求保留所有应用程序的指标 5 年，以便将来在可能的法律诉讼中进行分析。  
您应该使用哪种方法？

A. Grant the security team access to the logs in each Project  
B. Configure Stackdriver Monitoring for all Projects, and export to BigQuery  
C. Configure Stackdriver Monitoring for all Projects with the default retention policies  
D. Configure Stackdriver Monitoring for all Projects, and export to Google Cloud Storage  

[Discussion](/assets/gcp/discussion/26.md)

# 27

Your company has decided to build a backup replica of their on-premises user authentication PostgreSQL database on Google Cloud Platform. The database is 4
TB, and large updates are frequent. Replication requires private address space communication.
Which networking approach should you use?  
您的公司已决定在 Google Cloud Platform 上构建其本地用户身份验证 PostgreSQL 数据库的备份副本。该数据库为 4
TB，并且经常进行大量更新。复制需要私有地址空间通信。  
您应该使用哪种网络方法？  

A. Google Cloud Dedicated Interconnect  
B. Google Cloud VPN connected to the data center network  
C. A NAT and TLS translation gateway installed on-premises  
D. A Google Compute Engine instance with a VPN server installed connected to the data center network  

[Discussion](/assets/gcp/discussion/27.md)

# 28

Auditors visit your teams every 12 months and ask to review all the Google Cloud Identity and Access Management (Cloud IAM) policy changes in the previous 12 months. You want to streamline and expedite the analysis and audit process.  
What should you do?  
审计人员每 12 个月访问一次您的团队，并要求审查过去 12 个月内的所有 Google Cloud Identity and Access Management (Cloud IAM) 政策变更。您想简化和加快分析和审计流程。
您应该怎么做？  

A. Create custom Google Stackdriver alerts and send them to the auditor  
B. Enable Logging export to Google BigQuery and use ACLs and views to scope the data shared with the auditor  
C. Use cloud functions to transfer log entries to Google Cloud SQL and use ACLs and views to limit an auditor's view  
D. Enable Google Cloud Storage (GCS) log export to audit logs into a GCS bucket and delegate access to the bucket  

[Discussion](/assets/gcp/discussion/28.md)

# 29
You are designing a large distributed application with 30 microservices. Each of your distributed microservices needs to connect to a database back-end. You want to store the credentials securely.  
Where should you store the credentials?  
您正在设计一个包含 30 个微服务的大型分布式应用程序。每个分布式微服务都需要连接到数据库后端。您希望安全地存储凭据。   
您应该将凭据存储在哪里？  

A. In the source code  
B. In an environment variable  
C. In a secret management system  
D. In a config file that has restricted access through ACLs  

[Discussion](/assets/gcp/discussion/29.md)  

# 30

A lead engineer wrote a custom tool that deploys virtual machines in the legacy data center. He wants to migrate the custom tool to the new cloud environment.
You want to advocate for the adoption of Google Cloud Deployment Manager.  
What are two business risks of migrating to Cloud Deployment Manager? (Choose two.)  
一位首席工程师编写了一个自定义工具，用于在旧数据中心部署虚拟机。他希望将自定义工具迁移到新的云环境。  
您想倡导采用 Google Cloud Deployment Manager。  
迁移到 Cloud Deployment Manager 的两种业务风险是什么？（选择两个。）  

A. Cloud Deployment Manager uses Python  
B. Cloud Deployment Manager APIs could be deprecated in the future  
C. Cloud Deployment Manager is unfamiliar to the company's engineers  
D. Cloud Deployment Manager requires a Google APIs service account to run  
E. Cloud Deployment Manager can be used to permanently delete cloud resources  
F. Cloud Deployment Manager only supports automation of Google Cloud resources  

[Discussion](/assets/gcp/discussion/30.md)

# 31

A development manager is building a new application. He asks you to review his requirements and identify what cloud technologies he can use to meet them. The application must:  
1. Be based on open-source technology for cloud portability  
2. Dynamically scale compute capacity based on demand  
3. Support continuous software delivery  
4. Run multiple segregated copies of the same application stack  
5. Deploy application bundles using dynamic templates  
6. Route network traffic to specific services based on URL  
Which combination of technologies will meet all of his requirements?  

一位开发经理正在构建一个新应用程序。他请您审核他的需求，并确定可以使用哪些云技术来满足这些需求。该应用程序必须：  
1. 基于开源技术，实现云可移植性   
2. 根据需求动态扩展计算能力  
3. 支持持续软件交付  
4. 运行同一应用程序堆栈的多个独立副本    
5. 使用动态模板部署应用程序包  
6. 根据 URL 将网络流量路由到特定服务  
哪种技术组合能够满足他的所有需求？

A. Google Kubernetes Engine, Jenkins, and Helm    
B. Google Kubernetes Engine and Cloud Load Balancing  
C. Google Kubernetes Engine and Cloud Deployment Manager  
D. Google Kubernetes Engine, Jenkins, and Cloud Load Balancing  

[Discussion](/assets/gcp/discussion/31.md)  

# 32

You have created several pre-emptible Linux virtual machine instances using Google Compute Engine. You want to properly shut down your application before the virtual machines are preempted.  
What should you do?  
您已使用 Google Compute Engine 创建了多个可抢占的 Linux 虚拟机实例。您想在虚拟机被抢占之前正确关闭您的应用程序。  
您应该怎么做？  

A. Create a shutdown script named k99.shutdown in the /etc/rc.6.d/ directory  
B. Create a shutdown script registered as a xinetd service in Linux and configure a Stackdriver endpoint check to call the service  
C. Create a shutdown script and use it as the value for a new metadata entry with the key shutdown-script in the Cloud Platform Console when you create the new virtual machine instance  
D. Create a shutdown script, registered as a xinetd service in Linux, and use the gcloud compute instances add-metadata command to specify the service URL as the value for a new metadata entry with the key shutdown-script-url  

[Discussion](/assets/gcp/discussion/32.md)  

# 33

Your organization has a 3-tier web application deployed in the same network on Google Cloud Platform. Each tier (web, API, and database) scales independently of the others. Network traffic should flow through the web to the API tier and then on to the database tier. Traffic should not flow between the web and the database tier.  
How should you configure the network?  
您的组织在 Google Cloud Platform 上的同一网络中部署了一个三层 Web 应用。每个层（Web、API 和数据库）都独立于其他层进行扩展。网络流量应通过 Web 层流向 API 层，然后再流向数据库层。流量不应在 Web 层和数据库层之间流动。  
您应该如何配置网络？  

A. Add each tier to a different subnetwork  
B. Set up software based firewalls on individual VMs  
C. Add tags to each tier and set up routes to allow the desired traffic flow  
D. Add tags to each tier and set up firewall rules to allow the desired traffic flow  

[Discussion](/assets/gcp/discussion/33.md)  

# 34

Your development team has installed a new Linux kernel module on the batch servers in Google Compute Engine (GCE) virtual machines (VMs) to speed up the nightly batch process. Two days after the installation, 50% of the batch servers failed the nightly batch run. You want to collect details on the failure to pass back to the development team.  
Which three actions should you take? (Choose three.)  
您的开发团队在 Google Compute Engine (GCE) 虚拟机 (VM) 中的批处理服务器上安装了新的 Linux 内核模块，以加快夜间批处理过程。安装两天后，50% 的批处理服务器未能完成夜间批处理运行。您想要收集有关失败的详细信息，并将其传回开发团队。  
您应该采取哪三项措施？（选择三项。）  


A. Use Stackdriver Logging to search for the module log entries  
B. Read the debug GCE Activity log using the API or Cloud Console  
C. Use gcloud or Cloud Console to connect to the serial console and observe the logs  
D. Identify whether a live migration event of the failed server occurred, using in the activity log  
E. Adjust the Google Stackdriver timeline to match the failure time, and observe the batch server metrics  
F. Export a debug VM into an image, and run the image on a local server where kernel log messages will be displayed on the native screen  

[Discussion](/assets/gcp/discussion/34.md)  

# 35
Your company wants to try out the cloud with low risk. They want to archive approximately 100 TB of their log data to the cloud and test the analytics features available to them there, while also retaining that data as a long-term disaster recovery backup.  
Which two steps should you take? (Choose two.)  
您的公司希望以低风险的方式试用云服务。他们希望将大约 100 TB 的日志数据归档到云端，并测试可用的分析功能，同时保留这些数据作为长期灾难恢复备份。  
您应该采取哪两个步骤？（选择两个。）  

A. Load logs into Google BigQuery  
B. Load logs into Google Cloud SQL  
C. Import logs into Google Stackdriver  
D. Insert logs into Google Cloud Bigtable  
E. Upload log files into Google Cloud Storage  

[Discussion](/assets/gcp/discussion/35.md)

# 36

You created a pipeline that can deploy your source code changes to your infrastructure in instance groups for self-healing. One of the changes negatively affects your key performance indicator. You are not sure how to fix it, and investigation could take up to a week.  
What should you do?  

A. Log in to a server, and iterate on the fox locally  
B. Revert the source code change, and rerun the deployment pipeline  
C. Log into the servers with the bad code change, and swap in the previous code  
D. Change the instance group template to the previous one, and delete all instances  


您创建了一个管道，可以将源代码更改部署到实例组中的基础架构中，以实现自我修复。其中一项更改对您的关键绩效指标 (KPI) 产生了负面影响。您不确定如何修复该问题，调查可能需要长达一周的时间。
您应该怎么做？  

A. 登录服务器，在本地迭代  
B. 恢复源代码更改，并重新运行部署管道  
C. 登录到错误代码更改的服务器，并替换之前的代码  
D. 将实例组模板更改为之前的模板，并删除所有实例  

[Discussion](/assets/gcp/discussion/36.md)

# 37

Your organization wants to control IAM policies for different departments independently, but centrally.  
Which approach should you take?  

A. Multiple Organizations with multiple Folders  
B. Multiple Organizations, one for each department  
C. A single Organization with Folders for each department  
D. A single Organization with multiple projects, each with a central owner  

您的组织希望独立但集中地控制不同部门的 IAM 策略。  
您应该采用哪种方法？  

A. 具有多个文件夹的多个组织  
B. 多个组织，每个部门一个  
C. 一个组织，每个部门都有文件夹  
D. 一个组织有多个项目，每个项目都有一个中心所有者  

[Discussion](/assets/gcp/discussion/37.md)

# 38

您将自定义 Java 应用程序部署到 Google App Engine。部署失败，并显示以下堆栈跟踪信息。
您应该怎么做？
digest error 。。。
A. 上传丢失的 JAR 文件并重新部署您的应用程序。  
B. 对所有 JAR 文件进行数字签名并重新部署应用程序  
C. 使用 MD5 哈希值（而不是 SHA1）重新编译 CLoakedServlet 类  

You deploy your custom Java application to Google App Engine. It fails to deploy and gives you the following stack trace.  
What should you do?  
  
A. Upload missing JAR files and redeploy your application.  
B. Digitally sign all of your JAR files and redeploy your application  
C. Recompile the CLoakedServlet class using and MD5 hash instead of SHA1  

[Discussion](/assets/gcp/discussion/38.md)

# 39

You are designing a mobile chat application. You want to ensure people cannot spoof chat messages, by providing a message were sent by a specific user.
What should you do?  

A. Tag messages client side with the originating user identifier and the destination user.  
B. Encrypt the message client side using block-based encryption with a shared key.  
C. Use public key infrastructure (PKI) to encrypt the message client side using the originating user's private key.  
D. Use a trusted certificate authority to enable SSL connectivity between the client application and the server.  

您正在设计一款移动聊天应用程序。您想通过提供由特定用户发送的消息来确保人们无法伪造聊天消息。  
您应该怎么做？  

A. 使用原始用户标识符和目标用户标记客户端消息。  
B. 使用基于块的加密和共享密钥对消息客户端进行加密。  
C. 使用公钥基础设施（PKI）通过发起用户的私钥对消息客户端进行加密。  
D. 使用受信任的证书颁发机构来启用客户端应用程序和服务器之间的 SSL 连接。  

[Discussion](/assets/gcp/discussion/39.md)

# 40
As part of implementing their disaster recovery plan, your company is trying to replicate their production MySQL database from their private data center to their
GCP project using a Google Cloud VPN connection. They are experiencing latency issues and a small amount of packet loss that is disrupting the replication.
What should they do?

A. Configure their replication to use UDP.
B. Configure a Google Cloud Dedicated Interconnect.
C. Restore their database daily using Google Cloud SQL.
D. Add additional VPN connections and load balance them.
E. Send the replicated transaction to Google Cloud Pub/Sub.

作为实施灾难恢复计划的一部分，贵公司正尝试
使用 Google Cloud VPN 连接将生产环境的 MySQL 数据库从私有数据中心复制到 GCP 项目。然而，他们遇到了延迟问题和少量数据包丢失，导致复制中断。  
该怎么办？  

A. 配置它们的复制以使用 UDP。  
B. 配置 Google Cloud 专用互连。  
C. 使用 Google Cloud SQL 每天恢复他们的数据库。  
D. 添加额外的 VPN 连接并对其进行负载平衡。  
E. 将复制的交易发送到 Google Cloud Pub/Sub。  

[Discussion](/assets/gcp/discussion/40.md)

# 41

Your customer support tool logs all email and chat conversations to Cloud Bigtable for retention and analysis. What is the recommended approach for sanitizing this data of personally identifiable information or payment card information before initial storage?  

A. Hash all data using SHA256  
B. Encrypt all data using elliptic curve cryptography  
C. De-identify the data with the Cloud Data Loss Prevention API  
D. Use regular expressions to find and redact phone numbers, email addresses, and credit card numbers  


您的客户支持工具会将所有电子邮件和聊天对话记录到 Cloud Bigtable 中进行保留和分析。在初始存储之前，建议如何清理这些数据中的个人身份信息或支付卡信息？  
  
A. 使用 SHA256 对所有数据进行哈希处理  
B. 使用椭圆曲线密码术加密所有数据  
C. 使用 Cloud Data Loss Prevention API 对数据进行去标识化  
D. 使用正则表达式查找和编辑电话号码、电子邮件地址和信用卡号  

[Discussion](/assets/gcp/discussion/41.md)

# 42

You are using Cloud Shell and need to install a custom utility for use in a few weeks. Where can you store the file so it is in the default execution path and persists across sessions?  

A. ~/bin  
B. Cloud Storage  
C. /google/scripts  
D. /usr/local/bin  

您正在使用 Cloud Shell，并且需要安装一个自定义实用程序以供几周后使用。您可以将该文件存储在哪里，以便它位于默认执行路径中并在会话之间持久保存？  

A. ~/bin  
B. 云存储  
C./google/scripts​  
D. /usr/local/bin  

[Discussion](/assets/gcp/discussion/42.md)

# 43

You want to create a private connection between your instances on Compute Engine and your on-premises data center. You require a connection of at least 20
Gbps. You want to follow Google-recommended practices. How should you set up the connection?  

A. Create a VPC and connect it to your on-premises data center using Dedicated Interconnect.  
B. Create a VPC and connect it to your on-premises data center using a single Cloud VPN.  
C. Create a Cloud Content Delivery Network (Cloud CDN) and connect it to your on-premises data center using Dedicated Interconnect.  
D. Create a Cloud Content Delivery Network (Cloud CDN) and connect it to your on-premises datacenter using a single Cloud VPN.  

您想在 Compute Engine 上的实例和本地数据中心之间创建私有连接。您需要至少 20
Gbps 的连接速度。您希望遵循 Google 推荐的做法。您应该如何设置连接？  

A. 创建一个 VPC 并使用专用互连将其连接到您的本地数据中心。  
B. 创建一个 VPC 并使用单个 Cloud VPN 将其连接到您的本地数据中心。  
C. 创建云内容分发网络 (Cloud CDN) 并使用专用互连将其连接到您的本地数据中心。  
D. 创建云内容分发网络 (Cloud CDN) 并使用单个 Cloud VPN 将其连接到您的本地数据中心。  

[Discussion](/assets/gcp/discussion/43.md)

# 44

You are analyzing and defining business processes to support your startup's trial usage of GCP, and you don't yet know what consumer demand for your product will be. Your manager requires you to minimize GCP service costs and adhere to Google best practices. What should you do?  
  
A. Utilize free tier and sustained use discounts. Provision a staff position for service cost management.  
B. Utilize free tier and sustained use discounts. Provide training to the team about service cost management.  
C. Utilize free tier and committed use discounts. Provision a staff position for service cost management.  
D. Utilize free tier and committed use discounts. Provide training to the team about service cost management.  

您正在分析和定义业务流程，以支持您的初创公司试用 GCP，但您尚不清楚消费者对您的产品的需求。您的经理要求您尽量降低 GCP 服务成本，并遵循 Google 的最佳实践。您应该怎么做？

A. 利用免费套餐和持续使用折扣。配备一个员工岗位，负责服务成本管理。  
B. 利用免费套餐和持续使用折扣。为团队提供服务成本管理方面的培训。  
C. 利用免费套餐和承诺使用折扣。配备一名工作人员负责服务成本管理。  
D. 利用免费套餐和承诺使用折扣。为团队提供服务成本管理方面的培训。  


[Discussion](/assets/gcp/discussion/44.md)

# 45

You are building a continuous deployment pipeline for a project stored in a Git source repository and want to ensure that code changes can be verified before deploying to production. What should you do?  

A. Use Spinnaker to deploy builds to production using the red/black deployment strategy so that changes can easily be rolled back.  
B. Use Spinnaker to deploy builds to production and run tests on production deployments.  
C. Use Jenkins to build the staging branches and the master branch. Build and deploy changes to production for 10% of users before doing a complete rollout.  
D. Use Jenkins to monitor tags in the repository. Deploy staging tags to a staging environment for testing. After testing, tag the repository for production and deploy that to the production environment.  

您正在为存储在 Git 源码仓库中的项目构建持续部署流水线，并希望确保在部署到生产环境之前能够验证代码更改。您应该怎么做？  

答： 使用 Spinnaker 通过红/黑部署策略将构建部署到生产环境，以便轻松回滚更改。  
B. 使用 Spinnaker 将构建部署到生产环境并在生产部署上运行测试。  
C. 使用 Jenkins 构建暂存分支和主分支。在全面部署之前，先为 10% 的用户构建并部署变更到生产环境。  
D. 使用 Jenkins 监控代码库中的标签。将暂存标签部署到暂存环境进行测试。测试完成后，将代码库标记为生产环境，并将其部署到生产环境。  

[Discussion](/assets/gcp/discussion/45.md)

# 46

You have an outage in your Compute Engine managed instance group: all instances keep restarting after 5 seconds. You have a health check configured, but autoscaling is disabled. Your colleague, who is a Linux expert, offered to look into the issue. You need to make sure that he can access the VMs. What should you do?  

A. Grant your colleague the IAM role of project Viewer  
B. Perform a rolling restart on the instance group  
C. Disable the health check for the instance group. Add his SSH key to the project-wide SSH Keys  
D. Disable autoscaling for the instance group. Add his SSH key to the project-wide SSH Keys  

您的 Compute Engine 托管实例组发生故障：所有实例在 5 秒后不断重启。您已配置健康检查，但自动扩缩功能已禁用。您的同事是一位 Linux 专家，他主动提出帮忙调查此问题。您需要确保他能够访问虚拟机。您该怎么办？  

A. 授予您的同事项目查看者的 IAM 角色  
B. 对实例组执行滚动重启  
C. 禁用实例组的健康检查。将他的 SSH 密钥添加到项目范围的 SSH 密钥中  
D. 禁用实例组的自动缩放。将其 SSH 密钥添加到项目范围的 SSH 密钥中  

[Discussion](/assets/gcp/discussion/46.md)

# 47
Your company is migrating its on-premises data center into the cloud. As part of the migration, you want to integrate Google Kubernetes Engine (GKE) for workload orchestration. Parts of your architecture must also be PCI DSS-compliant. Which of the following is most accurate?  

A. App Engine is the only compute platform on GCP that is certified for PCI DSS hosting.  
B. GKE cannot be used under PCI DSS because it is considered shared hosting.  
C. GKE and GCP provide the tools you need to build a PCI DSS-compliant environment.  
D. All Google Cloud services are usable because Google Cloud Platform is certified PCI-compliant.  

您的公司正在将其本地数据中心迁移到云端。作为迁移的一部分，您希望集成 Google Kubernetes Engine (GKE) 来编排工作负载。您的部分架构还必须符合 PCI DSS 标准。以下哪项最准确？

答： App Engine 是 GCP 上唯一经过 PCI DSS 托管认证的计算平台。  
B. GKE 不能在 PCI DSS 下使用，因为它被视为共享托管。  
C. GKE 和 GCP 提供构建符合 PCI DSS 的环境所需的工具。  
D. 所有 Google Cloud 服务均可使用，因为 Google Cloud Platform 已通过 PCI 认证。  

[Discussion](/assets/gcp/discussion/47.md)

# 48
Your company has multiple on-premises systems that serve as sources for reporting. The data has not been maintained well and has become degraded over time.
You want to use Google-recommended practices to detect anomalies in your company data. What should you do?  

A. Upload your files into Cloud Storage. Use Cloud Datalab to explore and clean your data.  
B. Upload your files into Cloud Storage. Use Cloud Dataprep to explore and clean your data.  
C. Connect Cloud Datalab to your on-premises systems. Use Cloud Datalab to explore and clean your data.  
D. Connect Cloud Dataprep to your on-premises systems. Use Cloud Dataprep to explore and clean your data.  

您的公司拥有多个本地系统作为报告来源。这些数据维护不善，随着时间的推移，质量逐渐下降。  
您想使用 Google 推荐的做法来检测公司数据中的异常。您应该怎么做？  

A. 将您的文件上传到 Cloud Storage。使用 Cloud Datalab 探索和清理您的数据。  
B. 将文件上传到 Cloud Storage。使用 Cloud Dataprep 探索和清理数据。  
C. 将 Cloud Datalab 连接到您的本地系统。使用 Cloud Datalab 探索和清理您的数据。  
D. 将 Cloud Dataprep 连接到您的本地系统。使用 Cloud Dataprep 探索和清理您的数据。  

[Discussion](/assets/gcp/discussion/48.md)

# 49
Google Cloud Platform resources are managed hierarchically using organization, folders, and projects. When Cloud Identity and Access Management (IAM) policies exist at these different levels, what is the effective policy at a particular node of the hierarchy?  

A. The effective policy is determined only by the policy set at the node  
B. The effective policy is the policy set at the node and restricted by the policies of its ancestors  
C. The effective policy is the union of the policy set at the node and policies inherited from its ancestors  
D. The effective policy is the intersection of the policy set at the node and policies inherited from its ancestors  

Google Cloud Platform 资源使用组织、文件夹和项目进行分层管理。当 Cloud Identity and Access Management (IAM) 策略存在于这些不同层级时，该层级结构中特定节点的有效策略是什么？

A. 有效策略仅由节点上设置的策略决定  
B. 有效策略是在该节点设置的策略，并受其祖先节点的策略限制  
C. 有效策略是该节点的策略集和从其祖先继承的策略的并集  
D. 有效策略是该节点的策略集与从其祖先节点继承的策略的交集  

[Discussion](/assets/gcp/discussion/49.md)

# 50

You are migrating your on-premises solution to Google Cloud in several phases. You will use Cloud VPN to maintain a connection between your on-premises systems and Google Cloud until the migration is completed. You want to make sure all your on-premise systems remain reachable during this period. How should you organize your networking in Google Cloud?  

A. Use the same IP range on Google Cloud as you use on-premises  
B. Use the same IP range on Google Cloud as you use on-premises for your primary IP range and use a secondary range that does not overlap with the range you use on-premises  
C. Use an IP range on Google Cloud that does not overlap with the range you use on-premises  
D. Use an IP range on Google Cloud that does not overlap with the range you use on-premises for your primary IP range and use a secondary range with the same IP range as you use on-premises  

您正在分几个阶段将本地解决方案迁移到 Google Cloud。您将使用 Cloud VPN 来维护本地系统与 Google Cloud 之间的连接，直到迁移完成。您希望确保在此期间所有本地系统保持可访问。您应该如何在 Google Cloud 中组织您的网络？  

答： 在 Google Cloud 上使用与本地相同的 IP 范围  
B. 在 Google Cloud 上使用与本地相同的 IP 范围作为主要 IP 范围，并使用与本地使用的范围不重叠的次要范围  
C. 在 Google Cloud 上使用与您在本地使用的范围不重叠的 IP 范围  
D. 在 Google Cloud 上使用的 IP 范围与您在本地使用的主要 IP 范围不重叠，并使用与您在本地使用的 IP 范围相同的次要范围  


[Discussion](/assets/gcp/discussion/50.md)

# 51

[Discussion](/assets/gcp/discussion/51.md)

# 52

[Discussion](/assets/gcp/discussion/52.md)

# 53

[Discussion](/assets/gcp/discussion/53.md)

# 54

[Discussion](/assets/gcp/discussion/54.md)

# 55

[Discussion](/assets/gcp/discussion/55.md)

# 56

[Discussion](/assets/gcp/discussion/56.md)

# 57

[Discussion](/assets/gcp/discussion/57.md)

# 58

[Discussion](/assets/gcp/discussion/58.md)

# 59

[Discussion](/assets/gcp/discussion/59.md)

# 60

[Discussion](/assets/gcp/discussion/60.md)

# 61

[Discussion](/assets/gcp/discussion/61.md)

# 62

[Discussion](/assets/gcp/discussion/62.md)

# 63

[Discussion](/assets/gcp/discussion/63.md)

# 64

[Discussion](/assets/gcp/discussion/64.md)

# 65

[Discussion](/assets/gcp/discussion/65.md)

# 66

[Discussion](/assets/gcp/discussion/66.md)

# 67

[Discussion](/assets/gcp/discussion/67.md)

# 68

[Discussion](/assets/gcp/discussion/68.md)

# 69

[Discussion](/assets/gcp/discussion/69.md)

# 70

[Discussion](/assets/gcp/discussion/70.md)

# 71

[Discussion](/assets/gcp/discussion/71.md)

# 72

[Discussion](/assets/gcp/discussion/72.md)

# 73

[Discussion](/assets/gcp/discussion/73.md)

# 74

[Discussion](/assets/gcp/discussion/74.md)

# 75

[Discussion](/assets/gcp/discussion/75.md)

# 76

[Discussion](/assets/gcp/discussion/76.md)

# 77

[Discussion](/assets/gcp/discussion/77.md)

# 78

[Discussion](/assets/gcp/discussion/78.md)

# 79

[Discussion](/assets/gcp/discussion/79.md)

# 80

[Discussion](/assets/gcp/discussion/80.md)

# 81

[Discussion](/assets/gcp/discussion/81.md)

# 82

[Discussion](/assets/gcp/discussion/82.md)

# 83

[Discussion](/assets/gcp/discussion/83.md)

# 84

[Discussion](/assets/gcp/discussion/84.md)

# 85

[Discussion](/assets/gcp/discussion/85.md)

# 86

[Discussion](/assets/gcp/discussion/86.md)

# 87

[Discussion](/assets/gcp/discussion/87.md)

# 88

[Discussion](/assets/gcp/discussion/88.md)

# 89

[Discussion](/assets/gcp/discussion/89.md)

# 90

[Discussion](/assets/gcp/discussion/90.md)

# 91

[Discussion](/assets/gcp/discussion/91.md)

# 92

[Discussion](/assets/gcp/discussion/92.md)

# 93

[Discussion](/assets/gcp/discussion/93.md)

# 94

[Discussion](/assets/gcp/discussion/94.md)

# 95

[Discussion](/assets/gcp/discussion/95.md)

# 96

[Discussion](/assets/gcp/discussion/96.md)

# 97

[Discussion](/assets/gcp/discussion/97.md)

# 98

[Discussion](/assets/gcp/discussion/98.md)

# 99

[Discussion](/assets/gcp/discussion/99.md)

# 100

[Discussion](/assets/gcp/discussion/100.md)