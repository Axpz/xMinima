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
  

A. Configure private Google access for on-premises hosts only.  
B. Configure private Google access.  
C. Configure private services access.  
D. Configure serverless VPC access.    
  
  
[Discussion](/assets/gcp/discussion/151.md)  
[Answer and Votes](/assets/gcp/discussion/151.ans.html)  
[VPC access of App Engine Standard vs Flex](/assets/gcp/discussion/151.vs.html)  
  
# 152

Your company is planning to upload several important files to Cloud Storage. After the upload is completed, they want to verify that the uploaded content is identical to what they have on-premises. You want to minimize the cost and effort of performing this check. What should you do?          


A. 1. Use Linux shasum to compute a digest of files you want to upload. 2. Use gsutil -m to upload all the files to Cloud Storage. 3. Use gsutil cp to download the uploaded files. 4. Use Linux shasum to compute a digest of the downloaded files. 5. Compare the hashes.  
B. 1. Use gsutil -m to upload the files to Cloud Storage. 2. Develop a custom Java application that computes CRC32C hashes. 3. Use gsutil ls -L gs://[YOUR_BUCKET_NAME] to collect CRC32C hashes of the uploaded files. 4. Compare the hashes.  
C. 1. Use gsutil -m to upload all the files to Cloud Storage. 2. Use gsutil cp to download the uploaded files. 3. Use Linux diff to compare the content of the files.  
D. 1. Use gsutil -m to upload the files to Cloud Storage. 2. Use gsutil hash -c FILE_NAME to generate CRC32C hashes of all on-premises files. 3. Use gsutil ls -L gs://[YOUR_BUCKET_NAME] to collect CRC32C hashes of the uploaded files. 4. Compare the hashes.    
  
[Discussion](/assets/gcp/discussion/152.md)  
[Answer and Votes](/assets/gcp/discussion/152.ans.html)  

  
# 153

You have deployed an application on Anthos clusters (formerly Anthos GKE). According to the SRE practices at your company, you need to be alerted if request latency is above a certain threshold for a specified amount of time. What should you do?        


A. Install Anthos Service Mesh on your cluster. Use the Google Cloud Console to define a Service Level Objective (SLO), and create an alerting policy based on this SLO.  
B. Enable the Cloud Trace API on your project, and use Cloud Monitoring Alerts to send an alert based on the Cloud Trace metrics.   
C. Use Cloud Profiler to follow up the request latency. Create a custom metric in Cloud Monitoring based on the results of Cloud Profiler, and create an Alerting policy in case this metric exceeds the threshold.  
D. Configure Anthos Config Management on your cluster, and create a yaml file that defines the SLO and alerting policy you want to deploy in your cluster.    
  
[Discussion](/assets/gcp/discussion/153.md)  
[Answers and Votes](/assets/gcp/discussion/153.ans.html)  
  
# 154

Your company has a stateless web API that performs scientific calculations. The web API runs on a single Google Kubernetes Engine (GKE) cluster. The cluster is currently deployed in us-central1. Your company has expanded to offer your API to customers in Asia. You want to reduce the latency for users in Asia.  
What should you do?         


A. Create a second GKE cluster in asia-southeast1, and expose both APIs using a Service of type LoadBalancer. Add the public IPs to the Cloud DNS zone.  
B. Use a global HTTP(s) load balancer with Cloud CDN enabled.  
C. Create a second GKE cluster in asia-southeast1, and use kubemci to create a global HTTP(s) load balancer.  
D. Increase the memory and CPU allocated to the application in the cluster.    
  
  
[Discussion](/assets/gcp/discussion/154.md)  
[Answers and Votes](/assets/gcp/discussion/154.ans.html)  

  
# 155

You are migrating third-party applications from optimized on-premises virtual machines to Google Cloud. You are unsure about the optimum CPU and memory options. The applications have a consistent usage pattern across multiple weeks. You want to optimize resource usage for the lowest cost. What should you do?        


A. Create an instance template with the smallest available machine type, and use an image of the third-party application taken from a current on-premises virtual machine. Create a managed instance group that uses average CPU utilization to autoscale the number of instances in the group. Modify the average CPU utilization threshold to optimize the number of instances running.  
B. Create an App Engine flexible environment, and deploy the third-party application using a Dockerfile and a custom runtime. Set CPU and memory options similar to your application's current on-premises virtual machine in the app.yaml file.  
C. Create multiple Compute Engine instances with varying CPU and memory options. Install the Cloud Monitoring agent, and deploy the third-party application on each of them. Run a load test with high traffic levels on the application, and use the results to determine the optimal settings.  
D. Create a Compute Engine instance with CPU and memory options similar to your application's current on-premises virtual machine. Install the Cloud Monitoring agent, and deploy the third-party application. Run a load test with normal traffic levels on the application, and follow the Rightsizing Recommendations in the Cloud Console.    
  
[Discussion](/assets/gcp/discussion/155.md)  
[Answers and Votes](/assets/gcp/discussion/155.ans.html)  

  
# 156

Your company has a Google Cloud project that uses BigQuery for data warehousing. They have a VPN tunnel between the on-premises environment and Google Cloud that is configured with Cloud VPN. The security team wants to avoid data exfiltration by malicious insiders, compromised code, and accidental oversharing.
What should they do?        


A. Configure Private Google Access for on-premises only.  
B. Perform the following tasks: 1. Create a service account. 2. Give the BigQuery JobUser role and Storage Reader role to the service account. 3. Remove all other IAM access from the project.  
C. Configure VPC Service Controls and configure Private Google Access.  
D. Configure Private Google Access.    
  
[Discussion](/assets/gcp/discussion/156.md)  
[Answers and Votes](/assets/gcp/discussion/156.ans.html)  
[VPC Service Controls](/assets/gcp/discussion/156.vs.html)  

  
# 157

You are working at an institution that processes medical data. You are migrating several workloads onto Google Cloud. Company policies require all workloads to run on physically separated hardware, and workloads from different clients must also be separated. You created a sole-tenant node group and added a node for each client. You need to deploy the workloads on these dedicated hosts. What should you do?        


A. Add the node group name as a network tag when creating Compute Engine instances in order to host each workload on the correct node group.  
B. Add the node name as a network tag when creating Compute Engine instances in order to host each workload on the correct node.  
C. Use node affinity labels based on the node group name when creating Compute Engine instances in order to host each workload on the correct node group.  
D. Use node affinity labels based on the node name when creating Compute Engine instances in order to host each workload on the correct node.    
  
[Discussion](/assets/gcp/discussion/157.md)  
[Answers and Votes](/assets/gcp/discussion/157.ans.html)  

  
# 158

Your company's test suite is a custom C++ application that runs tests throughout each day on Linux virtual machines. The full test suite takes several hours to complete, running on a limited number of on-premises servers reserved for testing. Your company wants to move the testing infrastructure to the cloud, to reduce the amount of time it takes to fully test a change to the system, while changing the tests as little as possible.  
Which cloud infrastructure should you recommend?        

  
A. Google Compute Engine unmanaged instance groups and Network Load Balancer  
B. Google Compute Engine managed instance groups with auto-scaling  
C. Google Cloud Dataproc to run Apache Hadoop jobs to process each test  
D. Google App Engine with Google StackDriver for logging    
  
[Discussion](/assets/gcp/discussion/158.md)  
[Answers and Votes](/assets/gcp/discussion/158.ans.html)  

  
# 159

A lead software engineer tells you that his new application design uses websockets and HTTP sessions that are not distributed across the web servers. You want to help him ensure his application will run properly on Google Cloud Platform.  
What should you do?          

A. Help the engineer to convert his websocket code to use HTTP streaming  
B. Review the encryption requirements for websocket connections with the security team  
C. Meet with the cloud operations team and the engineer to discuss load balancer options  
D. Help the engineer redesign the application to use a distributed user session service that does not rely on websockets and HTTP sessions.    
  
[Discussion](/assets/gcp/discussion/159.md)  
[Answers and Votes](/assets/gcp/discussion/159.ans.html)  

  
# 160

The application reliability team at your company this added a debug feature to their backend service to send all server events to Google Cloud Storage for eventual analysis. The event records are at least 50 KB and at most 15 MB and are expected to peak at 3,000 events per second. You want to minimize data loss.  
Which process should you implement?        



A. ג€¢ Append metadata to file body ג€¢ Compress individual files ג€¢ Name files with serverName ג€" Timestamp ג€¢ Create a new bucket if bucket is older than 1 hour and save individual files to the new bucket. Otherwise, save files to existing bucket.  
B. ג€¢ Batch every 10,000 events with a single manifest file for metadata ג€¢ Compress event files and manifest file into a single archive file ג€¢ Name files using serverName ג€" EventSequence ג€¢ Create a new bucket if bucket is older than 1 day and save the single archive file to the new bucket. Otherwise, save the single archive file to existing bucket.  
C. ג€¢ Compress individual files ג€¢ Name files with serverName ג€" EventSequence ג€¢ Save files to one bucket ג€¢ Set custom metadata headers for each object after saving  
D. ג€¢ Append metadata to file body ג€¢ Compress individual files ג€¢ Name files with a random prefix pattern ג€¢ Save files to one bucket    
  
[Discussion](/assets/gcp/discussion/160.md)  
[Answers and Votes](/assets/gcp/discussion/160.ans.html)  

  
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
[Answers and Votes](/assets/gcp/discussion/161.ans.html)  

  
# 162

You want to make a copy of a production Linux virtual machine in the US-Central region. You want to manage and replace the copy easily if there are changes on the production virtual machine. You will deploy the copy as a new instance in a different project in the US-East region.  
What steps must you take?        
  

A. Use the Linux dd and netcat commands to copy and stream the root disk contents to a new virtual machine instance in the US-East region.  
B. Create a snapshot of the root disk and select the snapshot as the root disk when you create a new virtual machine instance in the US-East region.  
C. Create an image file from the root disk with Linux dd command, create a new virtual machine instance in the US-East region  
D. Create a snapshot of the root disk, create an image file in Google Cloud Storage from the snapshot, and create a new virtual machine instance in the US-East region using the image file the root disk.    
  
[Discussion](/assets/gcp/discussion/162.md)  
[Answers and Votes](/assets/gcp/discussion/162.ans.html)  

  
# 163

Your company runs several databases on a single MySQL instance. They need to take backups of a specific database at regular intervals. The backup activity needs to complete as quickly as possible and cannot be allowed to impact disk performance.  
How should you configure the storage?             
  
  

A. Configure a cron job to use the gcloud tool to take regular backups using persistent disk snapshots.  
B. Mount a Local SSD volume as the backup location. After the backup is complete, use gsutil to move the backup to Google Cloud Storage.  
C. Use gcsfise to mount a Google Cloud Storage bucket as a volume directly on the instance and write backups to the mounted location using mysqldump.  
D. Mount additional persistent disk volumes onto each virtual machine (VM) instance in a RAID10 array and use LVM to create snapshots to send to Cloud Storage    
  
[Discussion](/assets/gcp/discussion/163.md)  
[Answers and Votes](/assets/gcp/discussion/163.ans.html)  

  
# 164

You are helping the QA team to roll out a new load-testing tool to test the scalability of your primary cloud services that run on Google Compute Engine with Cloud Bigtable.  
Which three requirements should they include?       (Choose three.)  
    

A. Ensure that the load tests validate the performance of Cloud Bigtable  
B. Create a separate Google Cloud project to use for the load-testing environment  
C. Schedule the load-testing tool to regularly run against the production environment  
D. Ensure all third-party systems your services use is capable of handling high load  
E. Instrument the production services to record every transaction for replay by the load-testing tool  
F. Instrument the load-testing tool and the target services with detailed logging and metrics collection    
  
[Discussion](/assets/gcp/discussion/164.md)  
[Answers and Votes](/assets/gcp/discussion/164.ans.html)  

  
# 165

Your customer is moving their corporate applications to Google Cloud Platform. The security team wants detailed visibility of all projects in the organization. You provision the Google Cloud Resource Manager and set up yourself as the org admin.  
What Google Cloud Identity and Access Management (Cloud IAM) roles should you give to the security team?          

A. Org viewer, project owner  
B. Org viewer, project viewer  
C. Org admin, project browser  
D. Project owner, network admin    
  
[Discussion](/assets/gcp/discussion/165.md)  
[Answers and Votes](/assets/gcp/discussion/165.ans.html)  

  
# 166

Your company places a high value on being responsive and meeting customer needs quickly. Their primary business objectives are release speed and agility. You want to reduce the chance of security errors being accidentally introduced.  
Which two actions can you take?       (Choose two.)  
您的公司高度重视快速响应并满足客户需求。他们的主要业务目标是发布速度和敏捷性。您希望降低意外引入安全错误的可能性。  
您可以采取哪两项措施？（选择两项。）    

A. Ensure every code check-in is peer reviewed by a security SME  
B. Use source code security analyzers as part of the CI/CD pipeline  
C. Ensure you have stubs to unit test all interfaces between components  
D. Enable code signing and a trusted binary repository integrated with your CI/CD pipeline  
E. Run a vulnerability security scanner as part of your continuous-integration /continuous-delivery (CI/CD) pipeline    
  
[Discussion](/assets/gcp/discussion/166.md)  
[Answers and Votes](/assets/gcp/discussion/166.ans.html)  

  
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
[Answers and Votes](/assets/gcp/discussion/167.ans.html)  

  
# 168

Your marketing department wants to send out a promotional email campaign. The development team wants to minimize direct operation management. They project a wide range of possible customer responses, from 100 to 500,000 click-through per day. The link leads to a simple website that explains the promotion and collects user information and preferences.  
Which infrastructure should you recommend?       (Choose two.)  


A. Use Google App Engine to serve the website and Google Cloud Datastore to store user data.  
B. Use a Google Container Engine cluster to serve the website and store data to persistent disk.  
C. Use a managed instance group to serve the website and Google Cloud Bigtable to store user data.  
D. Use a single Compute Engine virtual machine (VM) to host a web server, backend by Google Cloud SQL.    
  
[Discussion](/assets/gcp/discussion/168.md)  
[Answers and Votes](/assets/gcp/discussion/168.ans.html)  

  
# 169

Your company just finished a rapid lift and shift to Google Compute Engine for your compute needs. You have another 9 months to design and deploy a more cloud-native solution. Specifically, you want a system that is no-ops and auto-scaling.  
Which two compute products should you choose?       (Choose two.)  
  

A. Compute Engine with containers  
B. Google Kubernetes Engine with containers  
C. Google App Engine Standard Environment  
D. Compute Engine with custom instance types  
E. Compute Engine with managed instance groups    
  
[Discussion](/assets/gcp/discussion/169.md)  
[Answers and Votes](/assets/gcp/discussion/169.ans.html)  

  
# 170

One of your primary business objectives is being able to trust the data stored in your application. You want to log all changes to the application data.  
How can you design your logging system to verify authenticity of your logs?          

A. Write the log concurrently in the cloud and on premises  
B. Use a SQL database and limit who can modify the log table  
C. Digitally sign each timestamp and log entry and store the signature  
D. Create a JSON dump of each log entry and store it in Google Cloud Storage  
  
[Discussion](/assets/gcp/discussion/170.md)  
[Answers and Votes](/assets/gcp/discussion/170.ans.html)  

  
# 171

Your company has a Google Workspace account and Google Cloud Organization. Some developers in the company have created Google Cloud projects outside of the Google Cloud Organization.  
You want to create an Organization structure that allows developers to create projects, but prevents them from modifying production projects. You want to manage policies for all projects centrally and be able to set more restrictive policies for production projects.  
You want to minimize disruption to users and developers when business needs change in the future. You want to follow Google-recommended practices. Now should you design the Organization structure?        
  

A. 1. Create a second Google Workspace account and Organization. 2. Grant all developers the Project Creator IAM role on the new Organization. 3. Move the developer projects into the new Organization. 4. Set the policies for all projects on both Organizations. 5. Additionally, set the production policies on the original Organization.  
B. 1. Create a folder under the Organization resource named ג€Production.ג€ 2. Grant all developers the Project Creator IAM role on the new Organization. 3. Move the developer projects into the new Organization. 4. Set the policies for all projects on the Organization. 5. Additionally, set the production policies on the ג€Productionג€ folder.  
C. 1. Create folders under the Organization resource named ג€Developmentג€ and ג€Production.ג€ 2. Grant all developers the Project Creator IAM role on the ג€Developmentג€ folder. 3. Move the developer projects into the ג€Developmentג€ folder. 4. Set the policies for all projects on the Organization. 5. Additionally, set the production policies on the ג€Productionג€ folder.  
D. 1. Designate the Organization for production projects only. 2. Ensure that developers do not have the Project Creator IAM role on the Organization. 3. Create development projects outside of the Organization using the developer Google Workspace accounts. 4. Set the policies for all projects on the Organization. 5. Additionally, set the production policies on the individual production projects.    
  
[Discussion](/assets/gcp/discussion/171.md)  
[Answers and Votes](/assets/gcp/discussion/171.ans.html)  

  
# 172

Your company has an application running on Compute Engine that allows users to play their favorite music. There are a fixed number of instances. Files are stored in Cloud Storage, and data is streamed directly to users. Users are reporting that they sometimes need to attempt to play popular songs multiple times before they are successful. You need to improve the performance of the application. What should you do?          


A. 1. Mount the Cloud Storage bucket using gcsfuse on all backend Compute Engine instances. 2. Serve music files directly from the backend Compute Engine instance.  
B. 1. Create a Cloud Filestore NFS volume and attach it to the backend Compute Engine instances. 2. Download popular songs in Cloud Filestore. 3. Serve music files directly from the backend Compute Engine instance.  
C. 1. Copy popular songs into CloudSQL as a blob. 2. Update application code to retrieve data from CloudSQL when Cloud Storage is overloaded.  
D. 1. Create a managed instance group with Compute Engine instances. 2. Create a global load balancer and configure it with two backends: ג—‹ Managed instance group ג—‹ Cloud Storage bucket 3. Enable Cloud CDN on the bucket backend.    
  
[Discussion](/assets/gcp/discussion/172.md)  
[Answers and Votes](/assets/gcp/discussion/172.ans.html)  

  
# 173
The operations team in your company wants to save Cloud VPN log events for one year. You need to configure the cloud infrastructure to save the logs. What should you do?          


A. Set up a filter in Cloud Logging and a Cloud Storage bucket as an export target for the logs you want to save.  
B. Enable the Compute Engine API, and then enable logging on the firewall rules that match the traffic you want to save.  
C. Set up a Cloud Logging Dashboard titled Cloud VPN Logs, and then add a chart that queries for the VPN metrics over a one-year time period.  
D. Set up a filter in Cloud Logging and a topic in Pub/Sub to publish the logs.    
  
[Discussion](/assets/gcp/discussion/173.md)  
[Answers and Votes](/assets/gcp/discussion/173.ans.html)  

  
# 174

You are working with a data warehousing team that performs data analysis. The team needs to process data from external partners, but the data contains personally identifiable information (PII). You need to process and store the data without storing any of the PIIE data. What should you do?        
  
     

A. Create a Dataflow pipeline to retrieve the data from the external sources. As part of the pipeline, use the Cloud Data Loss Prevention (Cloud DLP) API to remove any PII data. Store the result in BigQuery.  
B. Create a Dataflow pipeline to retrieve the data from the external sources. As part of the pipeline, store all non-PII data in BigQuery and store all PII data in a Cloud Storage bucket that has a retention policy set.  
C. Ask the external partners to upload all data on Cloud Storage. Configure Bucket Lock for the bucket. Create a Dataflow pipeline to read the data from the bucket. As part of the pipeline, use the Cloud Data Loss Prevention (Cloud DLP) API to remove any PII data. Store the result in BigQuery.  
D. Ask the external partners to import all data in your BigQuery dataset. Create a dataflow pipeline to copy the data into a new table. As part of the Dataflow bucket, skip all data in columns that have PII data    
  
[Discussion](/assets/gcp/discussion/174.md)  
[Answers and Votes](/assets/gcp/discussion/174.ans.html)  

  
# 175

You want to allow your operations team to store logs from all the production projects in your Organization, without including logs from other projects. All of the production projects are contained in a folder. You want to ensure that all logs for existing and new production projects are captured automatically. What should you do?          

A. Create an aggregated export on the Production folder. Set the log sink to be a Cloud Storage bucket in an operations project.  
B. Create an aggregated export on the Organization resource. Set the log sink to be a Cloud Storage bucket in an operations project.  
C. Create log exports in the production projects. Set the log sinks to be a Cloud Storage bucket in an operations project.  
D. Create log exports in the production projects. Set the log sinks to be BigQuery datasets in the production projects, and grant IAM access to the operations team to run queries on the datasets.    
  
[Discussion](/assets/gcp/discussion/175.md)  
[Answers and Votes](/assets/gcp/discussion/175.ans.html)  

  
# 176

Your company has an application that is running on multiple instances of Compute Engine. It generates 1 TB per day of logs. For compliance reasons, the logs need to be kept for at least two years. The logs need to be available for active query for 30 days. After that, they just need to be retained for audit purposes. You want to implement a storage solution that is compliant, minimizes costs, and follows Google-recommended practices. What should you do?          


  
A. 1. Install a Cloud Logging agent on all instances. 2. Create a sink to export logs into a regional Cloud Storage bucket. 3. Create an Object Lifecycle rule to move files into a Coldline Cloud Storage bucket after one month. 4. Configure a retention policy at the bucket level using bucket lock.  
B. 1. Write a daily cron job, running on all instances, that uploads logs into a Cloud Storage bucket. 2. Create a sink to export logs into a regional Cloud Storage bucket. 3. Create an Object Lifecycle rule to move files into a Coldline Cloud Storage bucket after one month.  
C. 1. Install a Cloud Logging agent on all instances. 2. Create a sink to export logs into a partitioned BigQuery table. 3. Set a time_partitioning_expiration of 30 days.  
D. 1. Create a daily cron job, running on all instances, that uploads logs into a partitioned BigQuery table. 2. Set a time_partitioning_expiration of 30 days.    
  
[Discussion](/assets/gcp/discussion/176.md)  
[Answers and Votes](/assets/gcp/discussion/176.ans.html)  

  
# 177

Your company has just recently activated Cloud Identity to manage users. The Google Cloud Organization has been configured as well. The security team needs to secure projects that will be part of the Organization. They want to prohibit IAM users outside the domain from gaining permissions from now on. What should they do?        

   

A. Configure an organization policy to restrict identities by domain.  
B. Configure an organization policy to block creation of service accounts.  
C. Configure Cloud Scheduler to trigger a Cloud Function every hour that removes all users that don't belong to the Cloud Identity domain from all projects.  
D. Create a technical user (e.g., crawler@yourdomain.com), and give it the project owner role at root organization level. Write a bash script that: ג€¢ Lists all the IAM rules of all projects within the organization. ג€¢ Deletes all users that do not belong to the company domain. Create a Compute Engine instance in a project within the Organization and configure gcloud to be executed with technical user credentials. Configure a cron job that executes the bash script every hour.    
  
[Discussion](/assets/gcp/discussion/177.md)  
[Answers and Votes](/assets/gcp/discussion/177.ans.html)  

  
# 178

Your company has an application running on Google Cloud that is collecting data from thousands of physical devices that are globally distributed. Data is published to Pub/Sub and streamed in real time into an SSD Cloud Bigtable cluster via a Dataflow pipeline. The operations team informs you that your Cloud Bigtable cluster has a hotspot, and queries are taking longer than expected. You need to resolve the problem and prevent it from happening in the future. What should you do?        
   

A. Advise your clients to use HBase APIs instead of NodeJS APIs.  
B. Delete records older than 30 days.  
C. Review your RowKey strategy and ensure that keys are evenly spread across the alphabet.  
D. Double the number of nodes you currently have.    
  
[Discussion](/assets/gcp/discussion/178.md)  
[Answers and Votes](/assets/gcp/discussion/178.ans.html)  

  
# 179

Your company has a Google Cloud project that uses BigQuery for data warehousing. There are some tables that contain personally identifiable information (PII). Only the compliance team may access the PII. The other information in the tables must be available to the data science team. You want to minimize cost and the time it takes to assign appropriate access to the tables. What should you do?        

      

A. 1. From the dataset where you have the source data, create views of tables that you want to share, excluding PII. 2. Assign an appropriate project-level IAM role to the members of the data science team. 3. Assign access controls to the dataset that contains the view.  
B. 1. From the dataset where you have the source data, create materialized views of tables that you want to share, excluding PII. 2. Assign an appropriate project-level IAM role to the members of the data science team. 3. Assign access controls to the dataset that contains the view.  
C. 1. Create a dataset for the data science team. 2. Create views of tables that you want to share, excluding PII. 3. Assign an appropriate project-level IAM role to the members of the data science team. 4. Assign access controls to the dataset that contains the view. 5. Authorize the view to access the source dataset.  
D. 1. Create a dataset for the data science team. 2. Create materialized views of tables that you want to share, excluding PII. 3. Assign an appropriate project-level IAM role to the members of the data science team. 4. Assign access controls to the dataset that contains the view. 5. Authorize the view to access the source dataset.    
  
  
[Discussion](/assets/gcp/discussion/179.md)  
[Answers and Votes](/assets/gcp/discussion/179.ans.html)  

  
# 180

Your operations team currently stores 10 TB of data in an object storage service from a third-party provider. They want to move this data to a Cloud Storage bucket as quickly as possible, following Google-recommended practices. They want to minimize the cost of this data migration. Which approach should they use?        


A. Use the gsutil mv command to move the data.  
B. Use the Storage Transfer Service to move the data.  
C. Download the data to a Transfer Appliance, and ship it to Google.  
D. Download the data to the on-premises data center, and upload it to the Cloud Storage bucket.    
  
  
[Discussion](/assets/gcp/discussion/180.md)  
[Answers and Votes](/assets/gcp/discussion/180.ans.html)  

  
# 181

You have a Compute Engine managed instance group that adds and removes Compute Engine instances from the group in response to the load on your application. The instances have a shutdown script that removes REDIS database entries associated with the instance. You see that many database entries have not been removed, and you suspect that the shutdown script is the problem. You need to ensure that the commands in the shutdown script are run reliably every time an instance is shut down. You create a Cloud Function to remove the database entries. What should you do next?        
您有一个 Compute Engine 托管实例组，该组会根据应用程序的负载情况，在组中添加和移除 Compute Engine 实例。这些实例有一个关闭脚本，用于删除与该实例关联的 REDIS 数据库条目。您发现许多数据库条目尚未删除，因此怀疑关闭脚本存在问题。您需要确保每次关闭实例时，关闭脚本中的命令都能可靠地运行。您创建了一个 Cloud Functions 函数来删除数据库条目。接下来应该做什么？    

A. Modify the shutdown script to wait for 30 seconds before triggering the Cloud Function.  
B. Do not use the Cloud Function. Modify the shutdown script to restart if it has not completed in 30 seconds.  
C. Set up a Cloud Monitoring sink that triggers the Cloud Function after an instance removal log message arrives in Cloud Logging.  
D. Modify the shutdown script to wait for 30 seconds and then publish a message to a Pub/Sub queue.    
  
  
[Discussion](/assets/gcp/discussion/181.md)  
[Answers and Votes](/assets/gcp/discussion/181.ans.html)  

  
# 182

You are managing several projects on Google Cloud and need to interact on a daily basis with BigQuery, Bigtable, and Kubernetes Engine using the gcloud CL tool. You are travelling a lot and work on different workstations during the week. You want to avoid having to manage the gcloud CLI manually. What should you do?        


A. Use Google Cloud Shell in the Google Cloud Console to interact with Google Cloud.  
B. Create a Compute Engine instance and install gcloud on the instance. Connect to this instance via SSH to always use the same gcloud installation when interacting with Google Cloud.  
C. Install gcloud on all of your workstations. Run the command gcloud components auto-update on each workstation  
D. Use a package manager to install gcloud on your workstations instead of installing it manually.    
  
[Discussion](/assets/gcp/discussion/182.md)  
[Answers and Votes](/assets/gcp/discussion/182.ans.html)  

  
# 183

Your company recently acquired a company that has infrastructure in Google Cloud. Each company has its own Google Cloud organization. Each company is using a Shared Virtual Private Cloud (VPC) to provide network connectivity for its applications. Some of the subnets used by both companies overlap. In order for both businesses to integrate, the applications need to have private network connectivity. These applications are not on overlapping subnets. You want to provide connectivity with minimal re-engineering. What should you do?        
 

A. Set up VPC peering and peer each Shared VPC together.  
B. Migrate the projects from the acquired company into your company's Google Cloud organization. Re-launch the instances in your companies Shared VPC.  
C. Set up a Cloud VPN gateway in each Shared VPC and peer Cloud VPNs.  
D. Configure SSH port forwarding on each application to provide connectivity between applications in the different Shared VPCs.    
  
[Discussion](/assets/gcp/discussion/183.md)  
[Answers and Votes](/assets/gcp/discussion/183.ans.html)  

  
# 184

You are managing several internal applications that are deployed on Compute Engine. Business users inform you that an application has become very slow over the past few days. You want to find the underlying cause in order to solve the problem. What should you do first?        


A. Inspect the logs and metrics from the instances in Cloud Logging and Cloud Monitoring.  
B. Change the Compute Engine Instances behind the application to a machine type with more CPU and memory.  
C. Restore a backup of the application database from a time before the application became slow.  
D. Deploy the applications on a managed instance group with autoscaling enabled. Add a load balancer in front of the managed instance group, and have the users connect to the IP of the load balancer.    
  
[Discussion](/assets/gcp/discussion/184.md)  
[Answers and Votes](/assets/gcp/discussion/184.ans.html)  

  
# 185

Your company has an application running as a Deployment in a Google Kubernetes Engine (GKE) cluster. When releasing new versions of the application via a rolling deployment, the team has been causing outages. The root cause of the outages is misconfigurations with parameters that are only used in production. You want to put preventive measures for this in the platform to prevent outages. What should you do?       


A. Configure liveness and readiness probes in the Pod specification.  
B. Configure health checks on the managed instance group.  
C. Create a Scheduled Task to check whether the application is available.  
D. Configure an uptime alert in Cloud Monitoring.    
  
[Discussion](/assets/gcp/discussion/185.md)  
[Answers and Votes](/assets/gcp/discussion/185.ans.html)  

  
# 186

Your company uses Google Kubernetes Engine (GKE) as a platform for all workloads. Your company has a single large GKE cluster that contains batch, stateful, and stateless workloads. The GKE cluster is configured with a single node pool with 200 nodes. Your company needs to reduce the cost of this cluster but does not want to compromise availability. What should you do?        

  
A. Create a second GKE cluster for the batch workloads only. Allocate the 200 original nodes across both clusters.  
B. Configure CPU and memory limits on the namespaces in the cluster. Configure all Pods to have a CPU and memory limits.  
C. Configure a HorizontalPodAutoscaler for all stateless workloads and for all compatible stateful workloads. Configure the cluster to use node auto scaling.  
D. Change the node pool to use preemptible VMs.    
  
[Discussion](/assets/gcp/discussion/186.md)  
[Answers and Votes](/assets/gcp/discussion/186.ans.html)  

  
# 187

Your company has a Google Cloud project that uses BigQuery for data warehousing on a pay-per-use basis. You want to monitor queries in real time to discover the most costly queries and which users spend the most. What should you do?        


A. 1. In the BigQuery dataset that contains all the tables to be queried, add a label for each user that can launch a query. 2. Open the Billing page of the project. 3. Select Reports. 4. Select BigQuery as the product and filter by the user you want to check.  
B. 1. Create a Cloud Logging sink to export BigQuery data access logs to BigQuery. 2. Perform a BigQuery query on the generated table to extract the information you need.  
C. 1. Create a Cloud Logging sink to export BigQuery data access logs to Cloud Storage. 2. Develop a Dataflow pipeline to compute the cost of queries split by users.  
D. 1. Activate billing export into BigQuery. 2. Perform a BigQuery query on the billing table to extract the information you need.    
  
[Discussion](/assets/gcp/discussion/187.md)  
[Answers and Votes](/assets/gcp/discussion/187.ans.html)  

  
# 188

Your company and one of its partners each have a Google Cloud project in separate organizations. Your company's project (prj-a) runs in Virtual Private Cloud(vpc-a). The partner's project (prj-b) runs in vpc-b. There are two instances running on vpc-a and one instance running on vpc-b. Subnets defined in both VPCs are not overlapping. You need to ensure that all instances communicate with each other via internal IPs, minimizing latency and maximizing throughput. What should you do?        
      

A. Set up a network peering between vpc-a and vpc-b.  
B. Set up a VPN between vpc-a and vpc-b using Cloud VPN.  
C. Configure IAP TCP forwarding on the instance in vpc-b, and then launch the following gcloud command from one of the instances in vpc-a gcloud: gcloud compute start-iap-tunnel INSTANCE_NAME_IN_VPC_8 22 \ --local-host-port=localhost:22  
D. 1. Create an additional instance in vpc-a. 2. Create an additional instance in vpc-b. 3. Install OpenVPN in newly created instances. 4. Configure a VPN tunnel between vpc-a and vpc-b with the help of OpenVPN.    
  
[Discussion](/assets/gcp/discussion/188.md)  
[Answers and Votes](/assets/gcp/discussion/188.ans.html)  

  
# 189

You want to store critical business information in Cloud Storage buckets. The information is regularly changed, but previous versions need to be referenced on a regular basis. You want to ensure that there is a record of all changes to any information in these buckets. You want to ensure that accidental edits or deletions can be easily rolled back. Which feature should you enable?          

  

A. Bucket Lock  
B. Object Versioning  
C. Object change notification  
D. Object Lifecycle Management    
  
[Discussion](/assets/gcp/discussion/189.md)  
[Answers and Votes](/assets/gcp/discussion/189.ans.html)  

  
# 190

You have a Compute Engine application that you want to autoscale when total memory usage exceeds 80%. You have installed the Cloud Monitoring agent and configured the autoscaling policy as follows:  
✑ Metric identifier: agent.googleapis.com/memory/percent_used  
✑ Filter: metric.label.state = 'used'  
✑ Target utilization level: 80    
✑ Target type: GAUGE  
You observe that the application does not scale under high load. You want to resolve this. What should you do?          


A. Change the Target type to DELTA_PER_MINUTE.  
B. Change the Metric identifier to agent.googleapis.com/memory/bytes_used.  
C. Change the filter to metric.label.state = 'used' AND metric.label.state = 'buffered' AND metric.label.state = 'cached' AND metric.label.state = 'slab'.  
D. Change the filter to metric.label.state = 'free' and the Target utilization to 20.    
  
[Discussion](/assets/gcp/discussion/190.md)  
[Answers and Votes](/assets/gcp/discussion/190.ans.html)  

  
# 191

You are deploying an application to Google Cloud. The application is part of a system. The application in Google Cloud must communicate over a private network with applications in a non-Google Cloud environment. The expected average throughput is 200 kbps. The business requires:
✑ as close to 100% system availability as possible
✑ cost optimization
You need to design the connectivity between the locations to meet the business requirements. What should you provision?        
       
  
A. An HA Cloud VPN gateway connected with two tunnels to an on-premises VPN gateway  
B. Two Classic Cloud VPN gateways connected to two on-premises VPN gateways Configure each Classic Cloud VPN gateway to have two tunnels, each connected to different on-premises VPN gateways  
C. Two HA Cloud VPN gateways connected to two on-premises VPN gateways Configure each HA Cloud VPN gateway to have two tunnels, each connected to different on-premises VPN gateways  
D. A single Cloud VPN gateway connected to an on-premises VPN gateway    
  
[Discussion](/assets/gcp/discussion/191.md)  
[Answers and Votes](/assets/gcp/discussion/191.ans.html)  

  
# 192

Your company has an application running on App Engine that allows users to upload music files and share them with other people. You want to allow users to upload files directly into Cloud Storage from their browser session. The payload should not be passed through the backend. What should you do?        


A.   
    1. Set a CORS configuration in the target Cloud Storage bucket where the base URL of the App Engine application is an allowed origin.  
    2. Use the Cloud Storage Signed URL feature to generate a POST URL.    
B.   
    1. Set a CORS configuration in the target Cloud Storage bucket where the base URL of the App Engine application is an allowed origin.  
    2. Assign the Cloud Storage WRITER role to users who upload files.    
C.   
    1. Use the Cloud Storage Signed URL feature to generate a POST URL.    
    2. Use App Engine default credentials to sign requests against Cloud Storage.    
D.   
    1. Assign the Cloud Storage WRITER role to users who upload files.    
    2. Use App Engine default credentials to sign requests against Cloud Storage.      
  
[Discussion](/assets/gcp/discussion/192.md)  
[Answers and Votes](/assets/gcp/discussion/192.ans.html)  

  
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
[Answers and Votes](/assets/gcp/discussion/193.ans.html)  

  
# 194

Your company is planning to migrate their Windows Server 2022 from their on-premises data center to Google Cloud. You need to bring the licenses that are currently in use in on-premises virtual machines into the target cloud environment. What should you do?        

A.   
    1. Create an image of the on-premises virtual machines and upload into Cloud Storage.    
    2. Import the image as a virtual disk on Compute Engine.    
B.   
    1. Create standard instances on Compute Engine.    
    2. Select as the OS the same Microsoft Windows version that is currently in use in the on-premises environment.    
C.   
    1. Create an image of the on-premises virtual machine.  
    2. Import the image as a virtual disk on Compute Engine.  
    3. Create a standard instance on Compute Engine, selecting as the OS the same Microsoft Windows version that is currently in use in the on-premises environment.    
    4. Attach a data disk that includes data that matches the created image.    
D. 
    1. Create an image of the on-premises virtual machines.    
    2. Import the image as a virtual disk on Compute Engine using --os=windows-2022-dc-v.    
    3. Create a sole-tenancy instance on Compute Engine that uses the imported disk as a boot disk.    
  
  
[Discussion](/assets/gcp/discussion/194.md)  
[Answers and Votes](/assets/gcp/discussion/194.ans.html)  

  
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
[Answers and Votes](/assets/gcp/discussion/195.ans.html)  

  
# 196

Your company wants to migrate their 10-TB on-premises database export into Cloud Storage. You want to minimize the time it takes to complete this activity and the overall cost. The bandwidth between the on-premises environment and Google Cloud is 1 Gbps. You want to follow Google-recommended practices. What should you do?          


A. Develop a Dataflow job to read data directly from the database and write it into Cloud Storage.  
B. Use the Data Transfer appliance to perform an offline migration.  
C. Use a commercial partner ETL solution to extract the data from the on-premises database and upload it into Cloud Storage.  
D. Upload the data with gcloud storage cp.    
  
  
[Discussion](/assets/gcp/discussion/196.md)  
[Answers and Votes](/assets/gcp/discussion/196.ans.html)  

  
# 197

You are working at a financial institution that stores mortgage loan approval documents on Cloud Storage. Any change to these approval documents must be uploaded as a separate approval file. You need to ensure that these documents cannot be deleted or overwritten for the next 5 years. What should you do?          


A. Create a retention policy on the bucket for the duration of 5 years. Create a lock on the retention policy.  
B. Create a retention policy organizational constraint constraints/storage.retentionPolicySeconds at the organization level. Set the duration to 5 years.  
C. Use a customer-managed key for the encryption of the bucket. Rotate the key after 5 years.  
D. Create a retention policy organizational constraint constraints/storage.retentionPolicySeconds at the project level. Set the duration to 5 years.    
  
[Discussion](/assets/gcp/discussion/197.md)  
[Answers and Votes](/assets/gcp/discussion/197.ans.html)  

  
# 198

Your company has decided to make a major revision of their API in order to create better experiences for their developers. They need to keep the old version of the API available and deployable, while allowing new customers and testers to try out the new API. They want to keep the same SSL and DNS records in place to serve both APIs.    

What should they do?          

  

A. Configure a new load balancer for the new version of the API  
B. Reconfigure old clients to use a new endpoint for the new API  
C. Have the old API forward traffic to the new API based on the path  
D. Use separate backend pools for each API path behind the load balancer    
  
  
[Discussion](/assets/gcp/discussion/198.md)  
[Answers and Votes](/assets/gcp/discussion/198.ans.html)  

  
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
[Answers and Votes](/assets/gcp/discussion/199.ans.html)  

  
# 200

Your company has a Google Cloud project that uses BigOuery for data warehousing. The VPN tunnel between the on-premises environment and Google Cloud is configured with Cloud VPN. Your security team wants to avoid data exfiltration by malicious insiders, compromised code, and accidental oversharing. What should you do?          

A. Configure Private Service Connect.  
B. Configure VPC Service Controls and configure Private Google Access for on-promises hosts.  
C. Create a service account, grant the BigQuery JobUser role and Storage Object Viewer role to the service account, and remove all other Identity and Access Management (IAM) access from the project.   
D. Configure Private Google Access.    
  
[Discussion](/assets/gcp/discussion/200.md)  
[Answers and Votes](/assets/gcp/discussion/200.ans.html)  

