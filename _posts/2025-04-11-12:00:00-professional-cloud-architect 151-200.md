---
layout: home
title: "professional cloud architect 151-200"
date: 2025-04-11 12:00:00 +0800
lastupdated: 2025-04-11 12:00:00 +0800
categories: cloud
tags: [ai,k8s,cloud]  
---
professional cloud architect 2025-04-11 12:00:00
  
# 151

Your company has a support ticketing solution that uses App Engine Standard. The project that contains the App Engine application already has a Virtual Private
Cloud (VPC) network fully connected to the company's on-premises environment through a Cloud VPN tunnel. You want to enable the App Engine application to communicate with a database that is running in the company's on-premises environment. What should you do?     
贵公司有一个使用 App Engine Standard 的支持工单解决方案。包含该 App Engine 应用的项目已拥有一个虚拟私有
云 (VPC) 网络，该网络通过 Cloud VPN 隧道完全连接到公司的本地环境。您想让该 App Engine 应用能够与公司本地环境中运行的数据库进行通信。您应该怎么做？    

A. Configure private Google access for on-premises hosts only.  
B. Configure private Google access.  
C. Configure private services access.  
D. Configure serverless VPC access.    
  
  
[Discussion](/assets/gcp/discussion/151.md)  
  
# 152

Your company is planning to upload several important files to Cloud Storage. After the upload is completed, they want to verify that the uploaded content is identical to what they have on-premises. You want to minimize the cost and effort of performing this check. What should you do?       

您的公司计划将几个重要文件上传到云存储。上传完成后，他们希望验证上传的内容是否与本地内容一致。您希望最大限度地减少执行此检查的成本和工作量。您应该怎么做？

A. 1. Use Linux shasum to compute a digest of files you want to upload. 2. Use gsutil -m to upload all the files to Cloud Storage. 3. Use gsutil cp to download the uploaded files. 4. Use Linux shasum to compute a digest of the downloaded files. 5. Compare the hashes.  
B. 1. Use gsutil -m to upload the files to Cloud Storage. 2. Develop a custom Java application that computes CRC32C hashes. 3. Use gsutil ls -L gs://[YOUR_BUCKET_NAME] to collect CRC32C hashes of the uploaded files. 4. Compare the hashes.  
C. 1. Use gsutil -m to upload all the files to Cloud Storage. 2. Use gsutil cp to download the uploaded files. 3. Use Linux diff to compare the content of the files.  
D. 1. Use gsutil -m to upload the files to Cloud Storage. 2. Use gsutil hash -c FILE_NAME to generate CRC32C hashes of all on-premises files. 3. Use gsutil ls -L gs://[YOUR_BUCKET_NAME] to collect CRC32C hashes of the uploaded files. 4. Compare the hashes.    
  
[Discussion](/assets/gcp/discussion/152.md)  
  
# 153

You have deployed an application on Anthos clusters (formerly Anthos GKE). According to the SRE practices at your company, you need to be alerted if request latency is above a certain threshold for a specified amount of time. What should you do?     
您已在 Anthos 集群（以前称为 Anthos GKE）上部署了一个应用程序。根据您公司的 SRE 实践，当请求延迟在指定时间内超过特定阈值时，您需要收到警报。您应该怎么做？    

A. Install Anthos Service Mesh on your cluster. Use the Google Cloud Console to define a Service Level Objective (SLO), and create an alerting policy based on this SLO.  
B. Enable the Cloud Trace API on your project, and use Cloud Monitoring Alerts to send an alert based on the Cloud Trace metrics.   
C. Use Cloud Profiler to follow up the request latency. Create a custom metric in Cloud Monitoring based on the results of Cloud Profiler, and create an Alerting policy in case this metric exceeds the threshold.  
D. Configure Anthos Config Management on your cluster, and create a yaml file that defines the SLO and alerting policy you want to deploy in your cluster.    
  
[Discussion](/assets/gcp/discussion/153.md)  
  
# 154

Your company has a stateless web API that performs scientific calculations. The web API runs on a single Google Kubernetes Engine (GKE) cluster. The cluster is currently deployed in us-central1. Your company has expanded to offer your API to customers in Asia. You want to reduce the latency for users in Asia.  
What should you do?      
贵公司有一个执行科学计算的无状态 Web API。该 Web API 在单个 Google Kubernetes Engine (GKE) 集群上运行。该集群目前部署在 us-central1 区域。贵公司已扩展 API 服务，向亚洲客户提供服务。您希望降低亚洲用户的延迟。  
您应该怎么做？    

A. Create a second GKE cluster in asia-southeast1, and expose both APIs using a Service of type LoadBalancer. Add the public IPs to the Cloud DNS zone.  
B. Use a global HTTP(s) load balancer with Cloud CDN enabled.  
C. Create a second GKE cluster in asia-southeast1, and use kubemci to create a global HTTP(s) load balancer.  
D. Increase the memory and CPU allocated to the application in the cluster.    
  
  
[Discussion](/assets/gcp/discussion/154.md)  
  
# 155

You are migrating third-party applications from optimized on-premises virtual machines to Google Cloud. You are unsure about the optimum CPU and memory options. The applications have a consistent usage pattern across multiple weeks. You want to optimize resource usage for the lowest cost. What should you do?     
您正在将第三方应用从优化的本地虚拟机迁移到 Google Cloud。您不确定最佳的 CPU 和内存选项。这些应用在数周内具有一致的使用模式。您希望优化资源使用率以降低成本。您应该怎么做？        

A. Create an instance template with the smallest available machine type, and use an image of the third-party application taken from a current on-premises virtual machine. Create a managed instance group that uses average CPU utilization to autoscale the number of instances in the group. Modify the average CPU utilization threshold to optimize the number of instances running.  
B. Create an App Engine flexible environment, and deploy the third-party application using a Dockerfile and a custom runtime. Set CPU and memory options similar to your application's current on-premises virtual machine in the app.yaml file.  
C. Create multiple Compute Engine instances with varying CPU and memory options. Install the Cloud Monitoring agent, and deploy the third-party application on each of them. Run a load test with high traffic levels on the application, and use the results to determine the optimal settings.  
D. Create a Compute Engine instance with CPU and memory options similar to your application's current on-premises virtual machine. Install the Cloud Monitoring agent, and deploy the third-party application. Run a load test with normal traffic levels on the application, and follow the Rightsizing Recommendations in the Cloud Console.    
  
[Discussion](/assets/gcp/discussion/155.md)  
  
# 156

Your company has a Google Cloud project that uses BigQuery for data warehousing. They have a VPN tunnel between the on-premises environment and Google
Cloud that is configured with Cloud VPN. The security team wants to avoid data exfiltration by malicious insiders, compromised code, and accidental oversharing.
What should they do?     

贵公司有一个 Google Cloud 项目，使用 BigQuery 进行数据仓储。他们在本地环境和 Google
Cloud 之间建立了一条 VPN 隧道，该隧道已配置 Cloud VPN。安全团队希望避免数据被恶意内部人员泄露、代码被盗以及意外过度共享。
他们应该怎么做？

A. Configure Private Google Access for on-premises only.  
B. Perform the following tasks: 1. Create a service account. 2. Give the BigQuery JobUser role and Storage Reader role to the service account. 3. Remove all other IAM access from the project.  
C. Configure VPC Service Controls and configure Private Google Access.  
D. Configure Private Google Access.    
  
[Discussion](/assets/gcp/discussion/156.md)  
  
# 157

You are working at an institution that processes medical data. You are migrating several workloads onto Google Cloud. Company policies require all workloads to run on physically separated hardware, and workloads from different clients must also be separated. You created a sole-tenant node group and added a node for each client. You need to deploy the workloads on these dedicated hosts. What should you do?     
您在一家处理医疗数据的机构工作。您正在将多个工作负载迁移到 Google Cloud。公司政策要求所有工作负载必须在物理上独立的硬件上运行，并且来自不同客户端的工作负载也必须隔离。您创建了一个单租户节点组，并为每个客户端添加了一个节点。您需要在这些专用主机上部署工作负载。您应该怎么做？    

A. Add the node group name as a network tag when creating Compute Engine instances in order to host each workload on the correct node group.  
B. Add the node name as a network tag when creating Compute Engine instances in order to host each workload on the correct node.  
C. Use node affinity labels based on the node group name when creating Compute Engine instances in order to host each workload on the correct node group.  
D. Use node affinity labels based on the node name when creating Compute Engine instances in order to host each workload on the correct node.    
  
[Discussion](/assets/gcp/discussion/157.md)  
  
# 158

Your company's test suite is a custom C++ application that runs tests throughout each day on Linux virtual machines. The full test suite takes several hours to complete, running on a limited number of on-premises servers reserved for testing. Your company wants to move the testing infrastructure to the cloud, to reduce the amount of time it takes to fully test a change to the system, while changing the tests as little as possible.  
Which cloud infrastructure should you recommend?     
一位首席软件工程师告诉您，他的新应用程序设计使用了未分布在各个 Web 服务器上的 WebSocket 和 HTTP 会话。您想帮助他确保该应用程序能够在 Google Cloud Platform 上正常运行。
您应该怎么做？    
  
A. Google Compute Engine unmanaged instance groups and Network Load Balancer  
B. Google Compute Engine managed instance groups with auto-scaling  
C. Google Cloud Dataproc to run Apache Hadoop jobs to process each test  
D. Google App Engine with Google StackDriver for logging    
  
[Discussion](/assets/gcp/discussion/158.md)  
  
# 159

A lead software engineer tells you that his new application design uses websockets and HTTP sessions that are not distributed across the web servers. You want to help him ensure his application will run properly on Google Cloud Platform.  
What should you do?       

A. Help the engineer to convert his websocket code to use HTTP streaming  
B. Review the encryption requirements for websocket connections with the security team  
C. Meet with the cloud operations team and the engineer to discuss load balancer options  
D. Help the engineer redesign the application to use a distributed user session service that does not rely on websockets and HTTP sessions.    
  
[Discussion](/assets/gcp/discussion/159.md)  
  
# 160

The application reliability team at your company this added a debug feature to their backend service to send all server events to Google Cloud Storage for eventual analysis. The event records are at least 50 KB and at most 15 MB and are expected to peak at 3,000 events per second. You want to minimize data loss.  
Which process should you implement?     
贵公司的应用可靠性团队在其后端服务中添加了一项调试功能，用于将所有服务器事件发送到 Google Cloud Storage 进行最终分析。事件记录大小至少为 50 KB，最多为 15 MB，预计峰值为每秒 3,000 个事件。您希望最大限度地减少数据丢失。  
您应该实施哪种流程？    

A. ג€¢ Append metadata to file body ג€¢ Compress individual files ג€¢ Name files with serverName ג€" Timestamp ג€¢ Create a new bucket if bucket is older than 1 hour and save individual files to the new bucket. Otherwise, save files to existing bucket.  
B. ג€¢ Batch every 10,000 events with a single manifest file for metadata ג€¢ Compress event files and manifest file into a single archive file ג€¢ Name files using serverName ג€" EventSequence ג€¢ Create a new bucket if bucket is older than 1 day and save the single archive file to the new bucket. Otherwise, save the single archive file to existing bucket.  
C. ג€¢ Compress individual files ג€¢ Name files with serverName ג€" EventSequence ג€¢ Save files to one bucket ג€¢ Set custom metadata headers for each object after saving  
D. ג€¢ Append metadata to file body ג€¢ Compress individual files ג€¢ Name files with a random prefix pattern ג€¢ Save files to one bucket    
  
[Discussion](/assets/gcp/discussion/160.md)  
  
# 161

A recent audit revealed that a new network was created in your GCP project. In this network, a GCE instance has an SSH port open to the world. You want to discover this network's origin.  
What should you do?     
最近的审计显示，您的 GCP 项目中创建了一个新网络。在该网络中，一个 GCE 实例向外界开放了一个 SSH 端口。您想查明该网络的来源。  
您应该怎么做？    

A. Search for Create VM entry in the Stackdriver alerting console  
B. Navigate to the Activity page in the Home section. Set category to Data Access and search for Create VM entry  
C. In the Logging section of the console, specify GCE Network as the logging section. Search for the Create Insert entry  
D. Connect to the GCE instance using project SSH keys. Identify previous logins in system logs, and match these with the project owners list    
  
[Discussion](/assets/gcp/discussion/161.md)  
  
# 162

You want to make a copy of a production Linux virtual machine in the US-Central region. You want to manage and replace the copy easily if there are changes on the production virtual machine. You will deploy the copy as a new instance in a different project in the US-East region.  
What steps must you take?     
您想要在美国中部地区复制一个生产 Linux 虚拟机。如果生产虚拟机发生更改，您希望能够轻松管理和替换该副本。您将在美国东部地区的另一个项目中将该副本部署为新实例。  
您需要采取哪些步骤？    

A. Use the Linux dd and netcat commands to copy and stream the root disk contents to a new virtual machine instance in the US-East region.  
B. Create a snapshot of the root disk and select the snapshot as the root disk when you create a new virtual machine instance in the US-East region.  
C. Create an image file from the root disk with Linux dd command, create a new virtual machine instance in the US-East region  
D. Create a snapshot of the root disk, create an image file in Google Cloud Storage from the snapshot, and create a new virtual machine instance in the US-East region using the image file the root disk.    
  
[Discussion](/assets/gcp/discussion/162.md)  
  
# 163

Your company runs several databases on a single MySQL instance. They need to take backups of a specific database at regular intervals. The backup activity needs to complete as quickly as possible and cannot be allowed to impact disk performance.  
How should you configure the storage?      
您的公司在单个 MySQL 实例上运行多个数据库。他们需要定期备份特定数据库。备份活动需要尽快完成，并且不能影响磁盘性能。  
您应该如何配置存储？    
  
  

A. Configure a cron job to use the gcloud tool to take regular backups using persistent disk snapshots.  
B. Mount a Local SSD volume as the backup location. After the backup is complete, use gsutil to move the backup to Google Cloud Storage.  
C. Use gcsfise to mount a Google Cloud Storage bucket as a volume directly on the instance and write backups to the mounted location using mysqldump.  
D. Mount additional persistent disk volumes onto each virtual machine (VM) instance in a RAID10 array and use LVM to create snapshots to send to Cloud Storage    
  
[Discussion](/assets/gcp/discussion/163.md)  
  
# 164

You are helping the QA team to roll out a new load-testing tool to test the scalability of your primary cloud services that run on Google Compute Engine with Cloud Bigtable.  
Which three requirements should they include?    (Choose three.)  
您正在帮助 QA 团队推出一款新的负载测试工具，用于测试在 Google Compute Engine 和 Cloud
Bigtable 上运行的主要云服务的可扩展性。  
该工具应包含哪三个要求？（选择三个。）    

A. Ensure that the load tests validate the performance of Cloud Bigtable  
B. Create a separate Google Cloud project to use for the load-testing environment  
C. Schedule the load-testing tool to regularly run against the production environment  
D. Ensure all third-party systems your services use is capable of handling high load  
E. Instrument the production services to record every transaction for replay by the load-testing tool  
F. Instrument the load-testing tool and the target services with detailed logging and metrics collection    
  
[Discussion](/assets/gcp/discussion/164.md)  
  
# 165

Your customer is moving their corporate applications to Google Cloud Platform. The security team wants detailed visibility of all projects in the organization. You provision the Google Cloud Resource Manager and set up yourself as the org admin.  
What Google Cloud Identity and Access Management (Cloud IAM) roles should you give to the security team?       

A. Org viewer, project owner  
B. Org viewer, project viewer  
C. Org admin, project browser  
D. Project owner, network admin    
  
[Discussion](/assets/gcp/discussion/165.md)  
  
# 166

Your company places a high value on being responsive and meeting customer needs quickly. Their primary business objectives are release speed and agility. You want to reduce the chance of security errors being accidentally introduced.  
Which two actions can you take?    (Choose two.)  
您的公司高度重视快速响应并满足客户需求。他们的主要业务目标是发布速度和敏捷性。您希望降低意外引入安全错误的可能性。  
您可以采取哪两项措施？（选择两项。）    

A. Ensure every code check-in is peer reviewed by a security SME  
B. Use source code security analyzers as part of the CI/CD pipeline  
C. Ensure you have stubs to unit test all interfaces between components  
D. Enable code signing and a trusted binary repository integrated with your CI/CD pipeline  
E. Run a vulnerability security scanner as part of your continuous-integration /continuous-delivery (CI/CD) pipeline    
  
[Discussion](/assets/gcp/discussion/166.md)  
  
# 167

You want to enable your running Google Kubernetes Engine cluster to scale as demand for your application changes.
What should you do?     
您希望使正在运行的 Google Kubernetes Engine 集群能够随着应用程序需求的变化而扩展。  
您应该怎么做？    

A. Add additional nodes to your Kubernetes Engine cluster using the following command: gcloud container clusters resize CLUSTER_Name ג€" -size 10  
B. Add a tag to the instances in the cluster with the following command: gcloud compute instances add-tags INSTANCE - -tags enable- autoscaling max-nodes-10  
C. Update the existing Kubernetes Engine cluster with the following command: gcloud alpha container clusters update mycluster - -enable- autoscaling - -min-nodes=1 - -max-nodes=10  
D. Create a new Kubernetes Engine cluster with the following command: gcloud alpha container clusters create mycluster - -enable- autoscaling - -min-nodes=1 - -max-nodes=10 and redeploy your application    
  
[Discussion](/assets/gcp/discussion/167.md)  
  
# 168

Your marketing department wants to send out a promotional email campaign. The development team wants to minimize direct operation management. They project a wide range of possible customer responses, from 100 to 500,000 click-through per day. The link leads to a simple website that explains the promotion and collects user information and preferences.  
Which infrastructure should you recommend?    (Choose two.)  
您的市场部门想要发送促销邮件。开发团队希望尽量减少直接运营管理。他们预测了各种可能的客户响应，每天的点击量从100到50万次不等。邮件链接指向一个简单的网站，该网站会解释促销活动并收集用户信息和偏好。  
您应该推荐哪种基础设施？（选择两项。）    

A. Use Google App Engine to serve the website and Google Cloud Datastore to store user data.  
B. Use a Google Container Engine cluster to serve the website and store data to persistent disk.  
C. Use a managed instance group to serve the website and Google Cloud Bigtable to store user data.  
D. Use a single Compute Engine virtual machine (VM) to host a web server, backend by Google Cloud SQL.    
  
[Discussion](/assets/gcp/discussion/168.md)  
  
# 169

Your company just finished a rapid lift and shift to Google Compute Engine for your compute needs. You have another 9 months to design and deploy a more cloud-native solution. Specifically, you want a system that is no-ops and auto-scaling.  
Which two compute products should you choose?    (Choose two.)  
您的公司刚刚完成了快速迁移到 Google Compute Engine 以满足您的计算需求。您还有 9 个月的时间来设计和部署更符合云原生需求的解决方案。具体来说，您需要一个无需运维且可自动扩展的系统。  
您应该选择哪两款计算产品？（选择两项。）    

A. Compute Engine with containers  
B. Google Kubernetes Engine with containers  
C. Google App Engine Standard Environment  
D. Compute Engine with custom instance types  
E. Compute Engine with managed instance groups    
  
[Discussion](/assets/gcp/discussion/169.md)  
  
# 170

One of your primary business objectives is being able to trust the data stored in your application. You want to log all changes to the application data.  
How can you design your logging system to verify authenticity of your logs?       

A. Write the log concurrently in the cloud and on premises  
B. Use a SQL database and limit who can modify the log table  
C. Digitally sign each timestamp and log entry and store the signature  
D. Create a JSON dump of each log entry and store it in Google Cloud Storage    
  
[Discussion](/assets/gcp/discussion/170.md)  
  
# 171

Your company has a Google Workspace account and Google Cloud Organization. Some developers in the company have created Google Cloud projects outside of the Google Cloud Organization.  
You want to create an Organization structure that allows developers to create projects, but prevents them from modifying production projects. You want to manage policies for all projects centrally and be able to set more restrictive policies for production projects.  
You want to minimize disruption to users and developers when business needs change in the future. You want to follow Google-recommended practices. Now should you design the Organization structure?     
您的公司拥有一个 Google Workspace 帐号和一个 Google Cloud Organization。公司中的一些开发者在 Google Cloud Organization 之外创建了 Google Cloud 项目。  
您希望创建一个组织结构，允许开发者创建项目，但禁止他们修改生产项目。您希望集中管理所有项目的政策，并能够为生产项目设置更严格的政策。  
您希望在未来业务需求发生变化时，最大限度地减少对用户和开发者的干扰。您希望遵循 Google 推荐的做法。现在您应该设计组织结构了吗？    

A. 1. Create a second Google Workspace account and Organization. 2. Grant all developers the Project Creator IAM role on the new Organization. 3. Move the developer projects into the new Organization. 4. Set the policies for all projects on both Organizations. 5. Additionally, set the production policies on the original Organization.  
B. 1. Create a folder under the Organization resource named ג€Production.ג€ 2. Grant all developers the Project Creator IAM role on the new Organization. 3. Move the developer projects into the new Organization. 4. Set the policies for all projects on the Organization. 5. Additionally, set the production policies on the ג€Productionג€ folder.  
C. 1. Create folders under the Organization resource named ג€Developmentג€ and ג€Production.ג€ 2. Grant all developers the Project Creator IAM role on the ג€Developmentג€ folder. 3. Move the developer projects into the ג€Developmentג€ folder. 4. Set the policies for all projects on the Organization. 5. Additionally, set the production policies on the ג€Productionג€ folder.  
D. 1. Designate the Organization for production projects only. 2. Ensure that developers do not have the Project Creator IAM role on the Organization. 3. Create development projects outside of the Organization using the developer Google Workspace accounts. 4. Set the policies for all projects on the Organization. 5. Additionally, set the production policies on the individual production projects.    
  
[Discussion](/assets/gcp/discussion/171.md)  
  
# 172

Your company has an application running on Compute Engine that allows users to play their favorite music. There are a fixed number of instances. Files are stored in Cloud Storage, and data is streamed directly to users. Users are reporting that they sometimes need to attempt to play popular songs multiple times before they are successful. You need to improve the performance of the application. What should you do?       

您的公司在 Compute Engine 上运行一个应用，允许用户播放自己喜欢的音乐。该应用的实例数量是固定的。文件存储在 Cloud Storage 中，数据直接流式传输给用户。用户反馈，他们有时需要多次尝试播放热门歌曲才能成功。您需要提升该应用的性能。您应该怎么做？    

A. 1. Mount the Cloud Storage bucket using gcsfuse on all backend Compute Engine instances. 2. Serve music files directly from the backend Compute Engine instance.  
B. 1. Create a Cloud Filestore NFS volume and attach it to the backend Compute Engine instances. 2. Download popular songs in Cloud Filestore. 3. Serve music files directly from the backend Compute Engine instance.  
C. 1. Copy popular songs into CloudSQL as a blob. 2. Update application code to retrieve data from CloudSQL when Cloud Storage is overloaded.  
D. 1. Create a managed instance group with Compute Engine instances. 2. Create a global load balancer and configure it with two backends: ג—‹ Managed instance group ג—‹ Cloud Storage bucket 3. Enable Cloud CDN on the bucket backend.    
  
[Discussion](/assets/gcp/discussion/172.md)  
  
# 173
The operations team in your company wants to save Cloud VPN log events for one year. You need to configure the cloud infrastructure to save the logs. What should you do?       

贵公司的运营团队希望保存一年的 Cloud VPN 日志事件。您需要配置云基础架构来保存这些日志。您应该怎么做？    

A. Set up a filter in Cloud Logging and a Cloud Storage bucket as an export target for the logs you want to save.  
B. Enable the Compute Engine API, and then enable logging on the firewall rules that match the traffic you want to save.  
C. Set up a Cloud Logging Dashboard titled Cloud VPN Logs, and then add a chart that queries for the VPN metrics over a one-year time period.  
D. Set up a filter in Cloud Logging and a topic in Pub/Sub to publish the logs.    
  
[Discussion](/assets/gcp/discussion/173.md)  
  
# 174

You are working with a data warehousing team that performs data analysis. The team needs to process data from external partners, but the data contains personally identifiable information (PII). You need to process and store the data without storing any of the PIIE data. What should you do?     

您正在与一个进行数据分析的数据仓库团队合作。该团队需要处理来自外部合作伙伴的数据，但这些数据包含个人身份信息 (PII)。您需要处理和存储这些数据，但不能存储任何 PIIE 数据。您应该怎么做？    

A. Create a Dataflow pipeline to retrieve the data from the external sources. As part of the pipeline, use the Cloud Data Loss Prevention (Cloud DLP) API to remove any PII data. Store the result in BigQuery.  
B. Create a Dataflow pipeline to retrieve the data from the external sources. As part of the pipeline, store all non-PII data in BigQuery and store all PII data in a Cloud Storage bucket that has a retention policy set.  
C. Ask the external partners to upload all data on Cloud Storage. Configure Bucket Lock for the bucket. Create a Dataflow pipeline to read the data from the bucket. As part of the pipeline, use the Cloud Data Loss Prevention (Cloud DLP) API to remove any PII data. Store the result in BigQuery.  
D. Ask the external partners to import all data in your BigQuery dataset. Create a dataflow pipeline to copy the data into a new table. As part of the Dataflow bucket, skip all data in columns that have PII data    
  
[Discussion](/assets/gcp/discussion/174.md)  
  
# 175

You want to allow your operations team to store logs from all the production projects in your Organization, without including logs from other projects. All of the production projects are contained in a folder. You want to ensure that all logs for existing and new production projects are captured automatically. What should you do?       

A. Create an aggregated export on the Production folder. Set the log sink to be a Cloud Storage bucket in an operations project.  
B. Create an aggregated export on the Organization resource. Set the log sink to be a Cloud Storage bucket in an operations project.  
C. Create log exports in the production projects. Set the log sinks to be a Cloud Storage bucket in an operations project.  
D. Create log exports in the production projects. Set the log sinks to be BigQuery datasets in the production projects, and grant IAM access to the operations team to run queries on the datasets.    
  
[Discussion](/assets/gcp/discussion/175.md)  
  
# 176

Your company has an application that is running on multiple instances of Compute Engine. It generates 1 TB per day of logs. For compliance reasons, the logs need to be kept for at least two years. The logs need to be available for active query for 30 days. After that, they just need to be retained for audit purposes. You want to implement a storage solution that is compliant, minimizes costs, and follows Google-recommended practices. What should you do?       

贵公司有一个在多个 Compute Engine 实例上运行的应用程序。它每天会生成 1 TB 的日志。出于合规性考虑，这些日志需要至少保存两年。这些日志需要可供主动查询 30 天。之后，只需将其保留用于审计目的。您希望实施一个合规、成本最低且遵循 Google 推荐做法的存储解决方案。您应该怎么做？    

A. 1. Install a Cloud Logging agent on all instances. 2. Create a sink to export logs into a regional Cloud Storage bucket. 3. Create an Object Lifecycle rule to move files into a Coldline Cloud Storage bucket after one month. 4. Configure a retention policy at the bucket level using bucket lock.  
B. 1. Write a daily cron job, running on all instances, that uploads logs into a Cloud Storage bucket. 2. Create a sink to export logs into a regional Cloud Storage bucket. 3. Create an Object Lifecycle rule to move files into a Coldline Cloud Storage bucket after one month.  
C. 1. Install a Cloud Logging agent on all instances. 2. Create a sink to export logs into a partitioned BigQuery table. 3. Set a time_partitioning_expiration of 30 days.  
D. 1. Create a daily cron job, running on all instances, that uploads logs into a partitioned BigQuery table. 2. Set a time_partitioning_expiration of 30 days.    
  
[Discussion](/assets/gcp/discussion/176.md)  
  
# 177

Your company has just recently activated Cloud Identity to manage users. The Google Cloud Organization has been configured as well. The security team needs to secure projects that will be part of the Organization. They want to prohibit IAM users outside the domain from gaining permissions from now on. What should they do?     
贵公司最近刚刚启用 Cloud Identity 来管理用户。Google Cloud 组织也已配置完毕。安全团队需要保护即将加入该组织的项目。他们希望从现在起禁止域外的 IAM 用户获取权限。他们应该怎么做？    

A. Configure an organization policy to restrict identities by domain.  
B. Configure an organization policy to block creation of service accounts.  
C. Configure Cloud Scheduler to trigger a Cloud Function every hour that removes all users that don't belong to the Cloud Identity domain from all projects.  
D. Create a technical user (e.g., crawler@yourdomain.com), and give it the project owner role at root organization level. Write a bash script that: ג€¢ Lists all the IAM rules of all projects within the organization. ג€¢ Deletes all users that do not belong to the company domain. Create a Compute Engine instance in a project within the Organization and configure gcloud to be executed with technical user credentials. Configure a cron job that executes the bash script every hour.    
  
[Discussion](/assets/gcp/discussion/177.md)  
  
# 178

Your company has an application running on Google Cloud that is collecting data from thousands of physical devices that are globally distributed. Data is published to Pub/Sub and streamed in real time into an SSD Cloud Bigtable cluster via a Dataflow pipeline. The operations team informs you that your Cloud
Bigtable cluster has a hotspot, and queries are taking longer than expected. You need to resolve the problem and prevent it from happening in the future. What should you do?     
贵公司在 Google Cloud 上运行着一个应用，该应用从分布在全球的数千台物理设备收集数据。数据发布到 Pub/Sub 平台，并通过 Dataflow 流水线实时传输到 SSD Cloud Bigtable 集群中。运营团队通知您，您的 Cloud Bigtable 集群存在热点，查询时间超出预期。您需要解决该问题并防止其再次发生。您应该怎么做？    

A. Advise your clients to use HBase APIs instead of NodeJS APIs.  
B. Delete records older than 30 days.  
C. Review your RowKey strategy and ensure that keys are evenly spread across the alphabet.  
D. Double the number of nodes you currently have.    
  
[Discussion](/assets/gcp/discussion/178.md)  
  
# 179

Your company has a Google Cloud project that uses BigQuery for data warehousing. There are some tables that contain personally identifiable information (PII).
Only the compliance team may access the PII. The other information in the tables must be available to the data science team. You want to minimize cost and the time it takes to assign appropriate access to the tables. What should you do?     
贵公司有一个 Google Cloud 项目，使用 BigQuery 进行数据仓储。其中一些表包含个人身份信息 (PII)。  
只有合规团队可以访问这些 PII。表中的其他信息必须向数据科学团队开放。您希望最大限度地降低分配适当表访问权限所需的成本和时间。您应该怎么做？    

A. 1. From the dataset where you have the source data, create views of tables that you want to share, excluding PII. 2. Assign an appropriate project-level IAM role to the members of the data science team. 3. Assign access controls to the dataset that contains the view.  
B. 1. From the dataset where you have the source data, create materialized views of tables that you want to share, excluding PII. 2. Assign an appropriate project-level IAM role to the members of the data science team. 3. Assign access controls to the dataset that contains the view.  
C. 1. Create a dataset for the data science team. 2. Create views of tables that you want to share, excluding PII. 3. Assign an appropriate project-level IAM role to the members of the data science team. 4. Assign access controls to the dataset that contains the view. 5. Authorize the view to access the source dataset.  
D. 1. Create a dataset for the data science team. 2. Create materialized views of tables that you want to share, excluding PII. 3. Assign an appropriate project-level IAM role to the members of the data science team. 4. Assign access controls to the dataset that contains the view. 5. Authorize the view to access the source dataset.    
  
  
[Discussion](/assets/gcp/discussion/179.md)  
  
# 180

Your operations team currently stores 10 TB of data in an object storage service from a third-party provider. They want to move this data to a Cloud Storage bucket as quickly as possible, following Google-recommended practices. They want to minimize the cost of this data migration. Which approach should they use?     
您的运营团队目前在第三方提供商的对象存储服务中存储了 10 TB 的数据。他们希望按照 Google 推荐的做法，尽快将这些数据迁移到 Cloud Storage 存储桶中。他们希望最大限度地降低数据迁移的成本。他们应该使用哪种方法？    

A. Use the gsutil mv command to move the data.  
B. Use the Storage Transfer Service to move the data.  
C. Download the data to a Transfer Appliance, and ship it to Google.  
D. Download the data to the on-premises data center, and upload it to the Cloud Storage bucket.    
  
  
[Discussion](/assets/gcp/discussion/180.md)  
  
# 181

You have a Compute Engine managed instance group that adds and removes Compute Engine instances from the group in response to the load on your application. The instances have a shutdown script that removes REDIS database entries associated with the instance. You see that many database entries have not been removed, and you suspect that the shutdown script is the problem. You need to ensure that the commands in the shutdown script are run reliably every time an instance is shut down. You create a Cloud Function to remove the database entries. What should you do next?     
您有一个 Compute Engine 托管实例组，该组会根据应用程序的负载情况，在组中添加和移除 Compute Engine 实例。这些实例有一个关闭脚本，用于删除与该实例关联的 REDIS 数据库条目。您发现许多数据库条目尚未删除，因此怀疑关闭脚本存在问题。您需要确保每次关闭实例时，关闭脚本中的命令都能可靠地运行。您创建了一个 Cloud Functions 函数来删除数据库条目。接下来应该做什么？    

A. Modify the shutdown script to wait for 30 seconds before triggering the Cloud Function.  
B. Do not use the Cloud Function. Modify the shutdown script to restart if it has not completed in 30 seconds.  
C. Set up a Cloud Monitoring sink that triggers the Cloud Function after an instance removal log message arrives in Cloud Logging.  
D. Modify the shutdown script to wait for 30 seconds and then publish a message to a Pub/Sub queue.    
  
  
[Discussion](/assets/gcp/discussion/181.md)  
  
# 182

You are managing several projects on Google Cloud and need to interact on a daily basis with BigQuery, Bigtable, and Kubernetes Engine using the gcloud CL tool. You are travelling a lot and work on different workstations during the week. You want to avoid having to manage the gcloud CLI manually. What should you do?     
您正在 Google Cloud 上管理多个项目，并且需要使用 gcloud CL 工具每天与 BigQuery、Bigtable 和 Kubernetes Engine 进行交互。您经常出差，并且在工作日使用不同的工作站。您希望避免手动管理 gcloud CLI。您应该怎么做？    

A. Use Google Cloud Shell in the Google Cloud Console to interact with Google Cloud.  
B. Create a Compute Engine instance and install gcloud on the instance. Connect to this instance via SSH to always use the same gcloud installation when interacting with Google Cloud.  
C. Install gcloud on all of your workstations. Run the command gcloud components auto-update on each workstation  
D. Use a package manager to install gcloud on your workstations instead of installing it manually.    
  
[Discussion](/assets/gcp/discussion/182.md)  
  
# 183

Your company recently acquired a company that has infrastructure in Google Cloud. Each company has its own Google Cloud organization. Each company is using a Shared Virtual Private Cloud (VPC) to provide network connectivity for its applications. Some of the subnets used by both companies overlap. In order for both businesses to integrate, the applications need to have private network connectivity. These applications are not on overlapping subnets. You want to provide connectivity with minimal re-engineering. What should you do?     
贵公司最近收购了一家在 Google Cloud 上拥有基础架构的公司。两家公司都有各自的 Google Cloud 组织。每家公司都使用共享虚拟私有云 (VPC) 为其应用程序提供网络连接。两家公司使用的部分子网存在重叠。为了使两家公司能够集成，应用程序需要具有私有网络连接。这些应用程序不在重叠的子网上。您希望以最少的重新设计提供连接。您应该怎么做？    

A. Set up VPC peering and peer each Shared VPC together.  
B. Migrate the projects from the acquired company into your company's Google Cloud organization. Re-launch the instances in your companies Shared VPC.  
C. Set up a Cloud VPN gateway in each Shared VPC and peer Cloud VPNs.  
D. Configure SSH port forwarding on each application to provide connectivity between applications in the different Shared VPCs.    
  
[Discussion](/assets/gcp/discussion/183.md)  
  
# 184

You are managing several internal applications that are deployed on Compute Engine. Business users inform you that an application has become very slow over the past few days. You want to find the underlying cause in order to solve the problem. What should you do first?     
您正在管理部署在 Compute Engine 上的多个内部应用。业务用户通知您，某个应用在过去几天变得非常缓慢。您想找到根本原因以解决问题。您首先应该做什么？    

A. Inspect the logs and metrics from the instances in Cloud Logging and Cloud Monitoring.  
B. Change the Compute Engine Instances behind the application to a machine type with more CPU and memory.  
C. Restore a backup of the application database from a time before the application became slow.  
D. Deploy the applications on a managed instance group with autoscaling enabled. Add a load balancer in front of the managed instance group, and have the users connect to the IP of the load balancer.    
  
[Discussion](/assets/gcp/discussion/184.md)  
  
# 185

Your company has an application running as a Deployment in a Google Kubernetes Engine (GKE) cluster. When releasing new versions of the application via a rolling deployment, the team has been causing outages. The root cause of the outages is misconfigurations with parameters that are only used in production. You want to put preventive measures for this in the platform to prevent outages. What should you do?    
贵公司有一个应用程序以 Deployment 的形式在 Google Kubernetes Engine (GKE) 集群中运行。在通过滚动部署发布该应用程序的新版本时，团队经常会遇到服务中断的情况。服务中断的根本原因是一些仅在生产环境中使用的参数配置错误。您希望在平台中引入预防措施，以防止服务中断。您应该怎么做？     

A. Configure liveness and readiness probes in the Pod specification.  
B. Configure health checks on the managed instance group.  
C. Create a Scheduled Task to check whether the application is available.  
D. Configure an uptime alert in Cloud Monitoring.    
  
[Discussion](/assets/gcp/discussion/185.md)  
  
# 186

Your company uses Google Kubernetes Engine (GKE) as a platform for all workloads. Your company has a single large GKE cluster that contains batch, stateful, and stateless workloads. The GKE cluster is configured with a single node pool with 200 nodes. Your company needs to reduce the cost of this cluster but does not want to compromise availability. What should you do?     
贵公司使用 Google Kubernetes Engine (GKE) 作为所有工作负载的平台。贵公司拥有一个大型 GKE 集群，其中包含批处理、有状态和无状态工作负载。该 GKE 集群配置了一个包含 200 个节点的单节点池。贵公司需要降低此集群的成本，但又不想牺牲可用性。您应该怎么做？    

A. Create a second GKE cluster for the batch workloads only. Allocate the 200 original nodes across both clusters.  
B. Configure CPU and memory limits on the namespaces in the cluster. Configure all Pods to have a CPU and memory limits.  
C. Configure a HorizontalPodAutoscaler for all stateless workloads and for all compatible stateful workloads. Configure the cluster to use node auto scaling.  
D. Change the node pool to use preemptible VMs.    
  
[Discussion](/assets/gcp/discussion/186.md)  
  
# 187

Your company has a Google Cloud project that uses BigQuery for data warehousing on a pay-per-use basis. You want to monitor queries in real time to discover the most costly queries and which users spend the most. What should you do?     
贵公司有一个 Google Cloud 项目，该项目使用 BigQuery 进行数据仓库管理，并按使用量付费。您希望实时监控查询，以发现成本最高的查询以及哪些用户花费最多。您应该怎么做？    

A. 1. In the BigQuery dataset that contains all the tables to be queried, add a label for each user that can launch a query. 2. Open the Billing page of the project. 3. Select Reports. 4. Select BigQuery as the product and filter by the user you want to check.  
B. 1. Create a Cloud Logging sink to export BigQuery data access logs to BigQuery. 2. Perform a BigQuery query on the generated table to extract the information you need.  
C. 1. Create a Cloud Logging sink to export BigQuery data access logs to Cloud Storage. 2. Develop a Dataflow pipeline to compute the cost of queries split by users.  
D. 1. Activate billing export into BigQuery. 2. Perform a BigQuery query on the billing table to extract the information you need.    
  
[Discussion](/assets/gcp/discussion/187.md)  
  
# 188

Your company and one of its partners each have a Google Cloud project in separate organizations. Your company's project (prj-a) runs in Virtual Private Cloud(vpc-a). The partner's project (prj-b) runs in vpc-b. There are two instances running on vpc-a and one instance running on vpc-b. Subnets defined in both VPCs are not overlapping. You need to ensure that all instances communicate with each other via internal IPs, minimizing latency and maximizing throughput. What should you do?     
您的公司及其合作伙伴分别在不同的组织中拥有一个 Google Cloud 项目。贵公司的项目 (prj-a) 在 Virtual Private Cloud
(vpc-a) 中运行。合作伙伴的项目 (prj-b) 在 vpc-b 中运行。vpc-a 上运行着两个实例，vpc-b 上运行着一个实例。两个 VPC 中定义的子网互不重叠。您需要确保所有实例都通过内部 IP 相互通信，从而最大限度地降低延迟并提高吞吐量。您应该怎么做？    

A. Set up a network peering between vpc-a and vpc-b.  
B. Set up a VPN between vpc-a and vpc-b using Cloud VPN.  
C. Configure IAP TCP forwarding on the instance in vpc-b, and then launch the following gcloud command from one of the instances in vpc-a gcloud: gcloud compute start-iap-tunnel INSTANCE_NAME_IN_VPC_8 22 \ --local-host-port=localhost:22  
D. 1. Create an additional instance in vpc-a. 2. Create an additional instance in vpc-b. 3. Install OpenVPN in newly created instances. 4. Configure a VPN tunnel between vpc-a and vpc-b with the help of OpenVPN.    
  
[Discussion](/assets/gcp/discussion/188.md)  
  
# 189

You want to store critical business information in Cloud Storage buckets. The information is regularly changed, but previous versions need to be referenced on a regular basis. You want to ensure that there is a record of all changes to any information in these buckets. You want to ensure that accidental edits or deletions can be easily rolled back. Which feature should you enable?       

您希望将关键业务信息存储在 Cloud Storage 存储桶中。这些信息会定期更改，但需要定期参考之前的版本。您希望确保这些存储桶中所有信息的所有更改都有记录。您希望确保意外的编辑或删除操作可以轻松回滚。您应该启用哪项功能？
  

A. Bucket Lock  
B. Object Versioning  
C. Object change notification  
D. Object Lifecycle Management    
  
[Discussion](/assets/gcp/discussion/189.md)  
  
# 190

You have a Compute Engine application that you want to autoscale when total memory usage exceeds 80%. You have installed the Cloud Monitoring agent and configured the autoscaling policy as follows:  
✑ Metric identifier: agent.googleapis.com/memory/percent_used  
✑ Filter: metric.label.state = 'used'  
✑ Target utilization level: 80    
✑ Target type: GAUGE  
You observe that the application does not scale under high load. You want to resolve this. What should you do?       

您有一个 Compute Engine 应用，希望在总内存使用量超过 80% 时自动扩缩。您已安装 Cloud Monitoring 代理并配置了以下自动扩缩策略：
✑ 指标标识符：agent.googleapis.com/memory/percent_used
✑ 过滤器：metric.label.state = 'used'
✑ 目标利用率级别：80
✑ 目标类型：GAUGE。
您发现该应用在高负载下无法扩缩。您想解决这个问题。您应该怎么做？

A. Change the Target type to DELTA_PER_MINUTE.  
B. Change the Metric identifier to agent.googleapis.com/memory/bytes_used.  
C. Change the filter to metric.label.state = 'used' AND metric.label.state = 'buffered' AND metric.label.state = 'cached' AND metric.label.state = 'slab'.  
D. Change the filter to metric.label.state = 'free' and the Target utilization to 20.    
  
[Discussion](/assets/gcp/discussion/190.md)  
  
# 191

You are deploying an application to Google Cloud. The application is part of a system. The application in Google Cloud must communicate over a private network with applications in a non-Google Cloud environment. The expected average throughput is 200 kbps. The business requires:
✑ as close to 100% system availability as possible
✑ cost optimization
You need to design the connectivity between the locations to meet the business requirements. What should you provision?     
  

您正在将一个应用程序部署到 Google Cloud。该应用程序是系统的一部分。Google Cloud 中的应用程序必须通过私有网络与非 Google Cloud 环境中的应用程序进行通信。预期平均吞吐量为 200 kbps。您的业务要求：  
✑ 尽可能接近 100% 的系统可用性  
✑ 成本优化。  
您需要设计不同位置之间的连接以满足业务需求。您应该配置哪些配置？    
  
A. An HA Cloud VPN gateway connected with two tunnels to an on-premises VPN gateway  
B. Two Classic Cloud VPN gateways connected to two on-premises VPN gateways Configure each Classic Cloud VPN gateway to have two tunnels, each connected to different on-premises VPN gateways  
C. Two HA Cloud VPN gateways connected to two on-premises VPN gateways Configure each HA Cloud VPN gateway to have two tunnels, each connected to different on-premises VPN gateways  
D. A single Cloud VPN gateway connected to an on-premises VPN gateway    
  
[Discussion](/assets/gcp/discussion/191.md)  
  
# 192

Your company has an application running on App Engine that allows users to upload music files and share them with other people. You want to allow users to upload files directly into Cloud Storage from their browser session. The payload should not be passed through the backend. What should you do?     
贵公司有一个在 App Engine 上运行的应用，允许用户上传音乐文件并与他人共享。您希望允许用户在浏览器会话中直接将文件上传到 Cloud Storage。有效负载不应通过后端传递。您应该怎么做？    
  
A. 1. Set a CORS configuration in the target Cloud Storage bucket where the base URL of the App Engine application is an allowed origin.
2. Use the Cloud Storage Signed URL feature to generate a POST URL.  
B. 1. Set a CORS configuration in the target Cloud Storage bucket where the base URL of the App Engine application is an allowed origin.
2. Assign the Cloud Storage WRITER role to users who upload files.  
C. 1. Use the Cloud Storage Signed URL feature to generate a POST URL.  
2. Use App Engine default credentials to sign requests against Cloud Storage.  
D. 1. Assign the Cloud Storage WRITER role to users who upload files.  
2. Use App Engine default credentials to sign requests against Cloud Storage.    
  
[Discussion](/assets/gcp/discussion/192.md)  
  
# 193

You are configuring the cloud network architecture for a newly created project in Google Cloud that will host applications in Compute Engine. Compute Engine virtual machine instances will be created in two different subnets (sub-a and sub-b) within a single region:  
• Instances in sub-a will have public IP addresses.  
• Instances in sub-b will have only private IP addresses.    

To download updated packages, instances must connect to a public repository outside the boundaries of Google Cloud. You need to allow sub-b to access the external repository. What should you do?       

您正在为 Google Cloud 中一个新创建的项目配置云网络架构，该项目将在 Compute Engine 中托管应用程序。Compute Engine 虚拟机实例将创建在单个区域内的两个不同子网（子网 a 和子网 b）中：  
• 子网 a 中的实例将拥有公共 IP 地址。  
• 子网 b 中的实例将仅拥有私有 IP 地址。    

A. Enable Private Google Access on sub-b.  
B. Configure Cloud NAT and select sub-b in the NAT mapping section.  
C. Configure a bastion host instance in sub-a to connect to instances in sub-b.  
D. Enable Identity-Aware Proxy for TCP forwarding for instances in sub-b.    
  
[Discussion](/assets/gcp/discussion/193.md)  
  
# 194

Your company is planning to migrate their Windows Server 2022 from their on-premises data center to Google Cloud. You need to bring the licenses that are currently in use in on-premises virtual machines into the target cloud environment. What should you do?     
贵公司计划将 Windows Server 2022 从本地数据中心迁移到 Google Cloud。您需要将当前在本地虚拟机中使用的许可证迁移到目标云环境中。您应该怎么做？    

A. 1. Create an image of the on-premises virtual machines and upload into Cloud Storage.  
2. Import the image as a virtual disk on Compute Engine.  
B. 1. Create standard instances on Compute Engine.  
2. Select as the OS the same Microsoft Windows version that is currently in use in the on-premises environment.  
C. 1. Create an image of the on-premises virtual machine.  
2. Import the image as a virtual disk on Compute Engine.  
3. Create a standard instance on Compute Engine, selecting as the OS the same Microsoft Windows version that is currently in use in the on-premises environment.  
4. Attach a data disk that includes data that matches the created image.  
D. 1. Create an image of the on-premises virtual machines.  
2. Import the image as a virtual disk on Compute Engine using --os=windows-2022-dc-v.  
3. Create a sole-tenancy instance on Compute Engine that uses the imported disk as a boot disk.    
  
  
[Discussion](/assets/gcp/discussion/194.md)  
  
# 195

You are deploying an application to Google Cloud. The application is part of a system. The application in Google Cloud must communicate over a private network with applications in a non-Google Cloud environment. The expected average throughput is 200 kbps. The business requires:    

• 99.99% system availability  
• cost optimization    

You need to design the connectivity between the locations to meet the business requirements. What should you provision?       
  

A. An HA Cloud VPN gateway connected with two tunnels to an on-premises VPN gateway.  
B. A Classic Cloud VPN gateway connected with two tunnels to an on-premises VPN gateway.  
C. Two HA Cloud VPN gateways connected to two on-premises VPN gateways. Configure each HA Cloud VPN gateway to have two tunnels, each connected to different on-premises VPN gateways.  
D. A Classic Cloud VPN gateway connected with one tunnel to an on-premises VPN gateway.    
  
[Discussion](/assets/gcp/discussion/195.md)  
  
# 196

Your company wants to migrate their 10-TB on-premises database export into Cloud Storage. You want to minimize the time it takes to complete this activity and the overall cost. The bandwidth between the on-premises environment and Google Cloud is 1 Gbps. You want to follow Google-recommended practices. What should you do?       

贵公司希望将其 10 TB 的本地数据库导出迁移到 Cloud Storage。您希望最大限度地缩短完成此操作所需的时间并降低总体成本。本地环境与 Google Cloud 之间的带宽为 1 Gbps。您希望遵循 Google 推荐的做法。您应该怎么做？    

A. Develop a Dataflow job to read data directly from the database and write it into Cloud Storage.  
B. Use the Data Transfer appliance to perform an offline migration.  
C. Use a commercial partner ETL solution to extract the data from the on-premises database and upload it into Cloud Storage.  
D. Upload the data with gcloud storage cp.    
  
  
[Discussion](/assets/gcp/discussion/196.md)  
  
# 197

You are working at a financial institution that stores mortgage loan approval documents on Cloud Storage. Any change to these approval documents must be uploaded as a separate approval file. You need to ensure that these documents cannot be deleted or overwritten for the next 5 years. What should you do?       

您在一家金融机构工作，该机构将抵押贷款审批文件存储在云存储中。这些审批文件的任何更改都必须作为单独的审批文件上传。您需要确保这些文件在未来 5 年内不会被删除或覆盖。您应该怎么做？    

A. Create a retention policy on the bucket for the duration of 5 years. Create a lock on the retention policy.  
B. Create a retention policy organizational constraint constraints/storage.retentionPolicySeconds at the organization level. Set the duration to 5 years.  
C. Use a customer-managed key for the encryption of the bucket. Rotate the key after 5 years.  
D. Create a retention policy organizational constraint constraints/storage.retentionPolicySeconds at the project level. Set the duration to 5 years.    
  
[Discussion](/assets/gcp/discussion/197.md)  
  
# 198

Your company has decided to make a major revision of their API in order to create better experiences for their developers. They need to keep the old version of the API available and deployable, while allowing new customers and testers to try out the new API. They want to keep the same SSL and DNS records in place to serve both APIs.    

What should they do?       

您的公司决定对其 API 进行重大修订，以便为开发人员提供更好的体验。他们需要保留旧版 API 的可用性和可部署性，同时允许新客户和测试人员试用新版 API。他们希望保留相同的 SSL 和 DNS 记录来服务这两个 API。    
  

A. Configure a new load balancer for the new version of the API  
B. Reconfigure old clients to use a new endpoint for the new API  
C. Have the old API forward traffic to the new API based on the path  
D. Use separate backend pools for each API path behind the load balancer    
  
  
[Discussion](/assets/gcp/discussion/198.md)  
  
# 199

You have a Compute Engine application that you want to autoscale when total memory usage exceeds 80%. You have installed the Cloud Monitoring agent and configured the autoscaling policy as follows:    
Metric identifier: agent.googleapis.com/memory/percent_used  
metric.label.state = 'used' AND  
metric.label.state = 'buffered' AND  
metric.label.state = 'cached' AND  
metric.label.state = 'slab'    

Filter:    

Target utilization level: 80  
Target type: GAUGE    

You observe that the application does not scale under high load. You want to resolve this. What should you do?     

A. Change the Target type to DELTA_PER_MINUTE.  
B. Change the Metric identifier to agent.googleapis.com/memory/bytes_used.  
C. Change the filter to metric.label.state = ‘used’.  
D. Change the filter to metric.label.state = ‘free’ and the Target utilization to 20.    
    
  
[Discussion](/assets/gcp/discussion/199.md)  
  
# 200

Your company has a Google Cloud project that uses BigOuery for data warehousing. The VPN tunnel between the on-premises environment and Google Cloud is configured with Cloud VPN. Your security team wants to avoid data exfiltration by malicious insiders, compromised code, and accidental oversharing. What should you do?       

A. Configure Private Service Connect.  
B. Configure VPC Service Controls and configure Private Google Access for on-promises hosts.  
C. Create a service account, grant the BigQuery JobUser role and Storage Object Viewer role to the service account, and remove all other Identity and Access Management (IAM) access from the project.   
D. Configure Private Google Access.    
  
[Discussion](/assets/gcp/discussion/200.md)  
