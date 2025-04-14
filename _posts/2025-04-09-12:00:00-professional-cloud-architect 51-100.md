---
layout: home
title: "professional cloud architect 51-100"
date: 2025-04-09 12:00:00 +0800
lastupdated: 2025-04-09 12:00:00 +0800
categories: cloud
tags: [ai,k8s,cloud]
---
professional cloud architect 2025-04-09 12:00:00


# 51

You have found an error in your App Engine application caused by missing Cloud Datastore indexes. You have created a YAML file with the required indexes and want to deploy these new indexes to Cloud Datastore. What should you do?        

A. Point gcloud datastore create-indexes to your configuration file  
B. Upload the configuration file to App Engine's default Cloud Storage bucket, and have App Engine detect the new indexes  
C. In the GCP Console, use Datastore Admin to delete the current indexes and upload the new configuration file  
D. Create an HTTP request to the built-in python module to send the index configuration file to your application       


[Discussion](/assets/gcp/discussion/51.md)  

# 52

You have an application that will run on Compute Engine. You need to design an architecture that takes into account a disaster recovery plan that requires your application to fail over to another region in case of a regional outage. What should you do?          

A. Deploy the application on two Compute Engine instances in the same project but in a different region. Use the first instance to serve traffic, and use the HTTP load balancing service to fail over to the standby instance in case of a disaster.  
B. Deploy the application on a Compute Engine instance. Use the instance to serve traffic, and use the HTTP load balancing service to fail over to an instance on your premises in case of a disaster.  
C. Deploy the application on two Compute Engine instance groups, each in the same project but in a different region. Use the first instance group to serve traffic, and use the HTTP load balancing service to fail over to the standby instance group in case of a disaster.  
D. Deploy the application on two Compute Engine instance groups, each in a separate project and a different region. Use the first instance group to serve traffic, and use the HTTP load balancing service to fail over to the standby instance group in case of a disaster.        

[Discussion](/assets/gcp/discussion/52.md)  
[Answers and Votes](/assets/gcp/discussion/52.ans.html)  

# 53

You are deploying an application on App Engine that needs to integrate with an on-premises database. For security purposes, your on-premises database must not be accessible through the public internet. What should you do?        

A. Deploy your application on App Engine standard environment and use App Engine firewall rules to limit access to the open on-premises database.  
B. Deploy your application on App Engine standard environment and use Cloud VPN to limit access to the on-premises database.  
C. Deploy your application on App Engine flexible environment and use App Engine firewall rules to limit access to the on-premises database.  
D. Deploy your application on App Engine flexible environment and use Cloud VPN to limit access to the on-premises database.    

[Discussion](/assets/gcp/discussion/53.md)  
[Answers and Votes](/assets/gcp/discussion/53.ans.html)  
[App Engine standard vs App Engine flexible](/assets/gcp/discussion/53.vs.html)  

# 54

You are working in a highly secured environment where public Internet access from the Compute Engine VMs is not allowed. You do not yet have a VPN connection to access an on-premises file server. You need to install specific software on a Compute Engine instance. How should you install the software?        

A. Upload the required installation files to Cloud Storage. Configure the VM on a subnet with a Private Google Access subnet. Assign only an internal IP address to the VM. Download the installation files to the VM using gsutil.  
B. Upload the required installation files to Cloud Storage and use firewall rules to block all traffic except the IP address range for Cloud Storage. Download the files to the VM using gsutil.  
C. Upload the required installation files to Cloud Source Repositories. Configure the VM on a subnet with a Private Google Access subnet. Assign only an internal IP address to the VM. Download the installation files to the VM using gcloud.  
D. Upload the required installation files to Cloud Source Repositories and use firewall rules to block all traffic except the IP address range for Cloud Source Repositories. Download the files to the VM using gsutil.       

[Discussion](/assets/gcp/discussion/54.md)  
[Answers and Votes](/assets/gcp/discussion/54.ans.html)  

# 55

Your company is moving 75 TB of data into Google Cloud. You want to use Cloud Storage and follow Google-recommended practices. What should you do?        

A. Move your data onto a Transfer Appliance. Use a Transfer Appliance Rehydrator to decrypt the data into Cloud Storage.  
B. Move your data onto a Transfer Appliance. Use Cloud Dataprep to decrypt the data into Cloud Storage.  
C. Install gsutil on each server that contains data. Use resumable transfers to upload the data into Cloud Storage.  
D. Install gsutil on each server containing data. Use streaming transfers to upload the data into Cloud Storage.    

[Discussion](/assets/gcp/discussion/55.md)  
[Answers and Votes](/assets/gcp/discussion/55.ans.html)  

# 56

You have an application deployed on Google Kubernetes Engine using a Deployment named echo-deployment. The deployment is exposed using a Service called echo-service. You need to perform an update to the application with minimal downtime to the application. What should you do?          

A. Use kubectl set image deployment/echo-deployment <new-image>

B. Use the rolling update functionality of the Instance Group behind the Kubernetes cluster  

C. Update the deployment yaml file with the new container image. Use kubectl delete deployment/echo-deployment and kubectl create ג€"f <yaml-file>  

D. Update the service yaml file which the new container image. Use kubectl delete service/echo-service and kubectl create ג€"f <yaml-file>    


[Discussion](/assets/gcp/discussion/56.md)  
[Answers and Votes](/assets/gcp/discussion/56.ans.html)  


# 57

Your company is using BigQuery as its enterprise data warehouse. Data is distributed over several Google Cloud projects. All queries on BigQuery need to be billed on a single project. You want to make sure that no query costs are incurred on the projects that contain the data. Users should be able to query the datasets, but not edit them.  
How should you configure users' access roles?          

A. Add all users to a group. Grant the group the role of BigQuery user on the billing project and BigQuery dataViewer on the projects that contain the data.  
B. Add all users to a group. Grant the group the roles of BigQuery dataViewer on the billing project and BigQuery user on the projects that contain the data.  
C. Add all users to a group. Grant the group the roles of BigQuery jobUser on the billing project and BigQuery dataViewer on the projects that contain the data.  
D. Add all users to a group. Grant the group the roles of BigQuery dataViewer on the billing project and BigQuery jobUser on the projects that contain the data.    

[Discussion](/assets/gcp/discussion/57.md)  

[Answers and Votes](/assets/gcp/discussion/57.ans.html)  

# 58

You have developed an application using Cloud ML Engine that recognizes famous paintings from uploaded images. You want to test the application and allow specific people to upload images for the next 24 hours. Not all users have a Google Account. How should you have users upload images?        


A. Have users upload the images to Cloud Storage. Protect the bucket with a password that expires after 24 hours.  
B. Have users upload the images to Cloud Storage using a signed URL that expires after 24 hours.  
C. Create an App Engine web application where users can upload images. Configure App Engine to disable the application after 24 hours. Authenticate users via Cloud Identity.  
D. Create an App Engine web application where users can upload images for the next 24 hours. Authenticate users via Cloud Identity.    


[Discussion](/assets/gcp/discussion/58.md)  
[Answers and Votes](/assets/gcp/discussion/58.ans.html)  


# 59

Your web application must comply with the requirements of the European Union's General Data Protection Regulation (GDPR). You are responsible for the technical architecture of your web application. What should you do?        


A. Ensure that your web application only uses native features and services of Google Cloud Platform, because Google already has various certifications and provides ג€pass-onג€ compliance when you use native features.  
B. Enable the relevant GDPR compliance setting within the GCPConsole for each of the services in use within your application.  
C. Ensure that Cloud Security Scanner is part of your test planning strategy in order to pick up any compliance gaps.  
D. Define a design for the security of data in your web application that meets GDPR requirements.  


[Discussion](/assets/gcp/discussion/59.md)  
[Answers and Votes](/assets/gcp/discussion/59.ans.html)  


# 60

You need to set up Microsoft SQL Server on GCP. Management requires that there's no downtime in case of a data center outage in any of the zones within a
GCP region. What should you do?           

A. Configure a Cloud SQL instance with high availability enabled.  
B. Configure a Cloud Spanner instance with a regional instance configuration.  
C. Set up SQL Server on Compute Engine, using Always On Availability Groups using Windows Failover Clustering. Place nodes in different subnets.  
D. Set up SQL Server Always On Availability Groups using Windows Failover Clustering. Place nodes in different zones.    

[Discussion](/assets/gcp/discussion/60.md)  
[Answers and Votes](/assets/gcp/discussion/60.ans.html)  


# 61

The development team has provided you with a Kubernetes Deployment file. You have no infrastructure yet and need to deploy the application. What should you do?      

A. Use gcloud to create a Kubernetes cluster. Use Deployment Manager to create the deployment.   
B. Use gcloud to create a Kubernetes cluster. Use kubectl to create the deployment.  
C. Use kubectl to create a Kubernetes cluster. Use Deployment Manager to create the deployment.  
D. Use kubectl to create a Kubernetes cluster. Use kubectl to create the deployment.    

[Discussion](/assets/gcp/discussion/61.md)  
[Answers and Votes](/assets/gcp/discussion/61.ans.html)  


# 62

You need to evaluate your team readiness for a new GCP project. You must perform the evaluation and create a skills gap plan which incorporates the business goal of cost optimization. Your team has deployed two GCP projects successfully to date. What should you do?        

A. Allocate budget for team training. Set a deadline for the new GCP project.  
B. Allocate budget for team training. Create a roadmap for your team to achieve Google Cloud certification based on job role.  
C. Allocate budget to hire skilled external consultants. Set a deadline for the new GCP project.  
D. Allocate budget to hire skilled external consultants. Create a roadmap for your team to achieve Google Cloud certification based on job role.    

[Discussion](/assets/gcp/discussion/62.md)  
[Answers and Votes](/assets/gcp/discussion/62.ans.html)  


# 63

You are designing an application for use only during business hours. For the minimum viable product release, you'd like to use a managed product that automatically `scales to zero` so you don't incur costs when there is no activity.  
Which primary compute resource should you choose?           

A. Cloud Functions  
B. Compute Engine  
C. Google Kubernetes Engine  
D. AppEngine flexible environment    

[Discussion](/assets/gcp/discussion/63.md)  
[Answers and Votes](/assets/gcp/discussion/63.ans.html)  


# 64

You are creating an App Engine application that uses Cloud Datastore as its persistence layer. You need to retrieve several root entities for which you have the identifiers. You want to minimize the overhead in operations performed by Cloud Datastore. What should you do?           

A. Create the Key object for each Entity and run a batch get operation  
B. Create the Key object for each Entity and run multiple get operations, one operation for each entity  
C. Use the identifiers to create a query filter and run a batch query operation  
D. Use the identifiers to create a query filter and run multiple query operations, one operation for each entity    

[Discussion](/assets/gcp/discussion/64.md)  
[Answers and Votes](/assets/gcp/discussion/64.ans.html)  

# 65

You need to upload files from your on-premises environment to Cloud Storage. You want the files to be encrypted on Cloud Storage using customer-supplied encryption keys. What should you do?         

A. Supply the encryption key in a .boto configuration file. Use gsutil to upload the files.  
B. Supply the encryption key using gcloud config. Use gsutil to upload the files to that bucket.  
C. Use gsutil to upload the files, and use the flag --encryption-key to supply the encryption key.  
D. Use gsutil to create a bucket, and use the flag --encryption-key to supply the encryption key. Use gsutil to upload the files to that bucket.    

[Discussion](/assets/gcp/discussion/65.md)  
[Answers and Votes](/assets/gcp/discussion/65.ans.html)  


# 66

Your customer wants to capture multiple GBs of aggregate real-time key performance indicators (KPIs) from their game servers running on Google Cloud Platform and monitor the KPIs with low latency. How should they capture the KPIs?         

A. Store time-series data from the game servers in Google Bigtable, and view it using Google Data Studio.  
B. Output custom metrics to Stackdriver from the game servers, and create a Dashboard in Stackdriver Monitoring Console to view them.  
C. Schedule BigQuery load jobs to ingest analytics files uploaded to Cloud Storage every ten minutes, and visualize the results in Google Data Studio.  
D. Insert the KPIs into Cloud Datastore entities, and run ad hoc analysis and visualizations of them in Cloud Datalab.    

[Discussion](/assets/gcp/discussion/66.md)  
[Answers and Votes](/assets/gcp/discussion/66.ans.html)  


# 67

You have a Python web application with many dependencies that requires 0.1 CPU cores and 128 MB of memory to operate in production. You want to monitor and maximize machine utilization. You also want to reliably deploy new versions of the application. Which set of steps should you take?        

A. Perform the following: 1. Create a managed instance group with f1-micro type machines. 2. Use a startup script to clone the repository, check out the production branch, install the dependencies, and start the Python app. 3. Restart the instances to automatically deploy new production releases.  
B. Perform the following: 1. Create a managed instance group with n1-standard-1 type machines. 2. Build a Compute Engine image from the production branch that contains all of the dependencies and automatically starts the Python app. 3. Rebuild the Compute Engine image, and update the instance template to deploy new production releases.  
C. Perform the following: 1. Create a Google Kubernetes Engine (GKE) cluster with n1-standard-1 type machines. 2. Build a Docker image from the production branch with all of the dependencies, and tag it with the version number. 3. Create a Kubernetes Deployment with the imagePullPolicy set to 'IfNotPresent' in the staging namespace, and then promote it to the production namespace after testing.  
D. Perform the following: 1. Create a GKE cluster with n1-standard-4 type machines. 2. Build a Docker image from the master branch with all of the dependencies, and tag it with 'latest'. 3. Create a Kubernetes Deployment in the default namespace with the imagePullPolicy set to 'Always'. Restart the pods to automatically deploy new production releases.    

[Discussion](/assets/gcp/discussion/67.md)  
[Answers and Votes](/assets/gcp/discussion/67.ans.html)  


# 68

Your company wants to start using Google Cloud resources but wants to retain their on-premises Active Directory domain controller for identity management.
What should you do?        
您的公司想要开始使用 Google Cloud 资源，但希望保留其本地 Active Directory 域控制器进行身份管理。  
您应该怎么做？    

A. Use the Admin Directory API to authenticate against the Active Directory domain controller.  
B. Use Google Cloud Directory Sync to synchronize Active Directory usernames with cloud identities and configure SAML SSO.  
C. Use Cloud Identity-Aware Proxy configured to use the on-premises Active Directory domain controller as an identity provider.  
D. Use Compute Engine to create an Active Directory (AD) domain controller that is a replica of the on-premises AD domain controller using Google Cloud Directory Sync.    

[Discussion](/assets/gcp/discussion/68.md)  
[Answers and Votes](/assets/gcp/discussion/68.ans.html)  


# 69

You are running a cluster on Kubernetes Engine (GKE) to serve a web application. Users are reporting that a specific part of the application is not responding anymore. You notice that all pods of your deployment keep restarting after 2 seconds. The application writes logs to standard output. You want to inspect the logs to find the cause of the issue. Which approach can you take?        

A. Review the Stackdriver logs for each Compute Engine instance that is serving as a node in the cluster.  
B. Review the Stackdriver logs for the specific GKE container that is serving the unresponsive part of the application.  
C. Connect to the cluster using gcloud credentials and connect to a container in one of the pods to read the logs.  
D. Review the Serial Port logs for each Compute Engine instance that is serving as a node in the cluster.    

[Discussion](/assets/gcp/discussion/69.md)  
[Answers and Votes](/assets/gcp/discussion/69.ans.html)  


# 70

You are using a single Cloud SQL instance to serve your application from a specific zone. You want to introduce high availability. What should you do?        

A. Create a read replica instance in a different region  
B. Create a failover replica instance in a different region  
C. Create a read replica instance in the same region, but in a different zone  
D. Create a failover replica instance in the same region, but in a different zone    

[Discussion](/assets/gcp/discussion/70.md)  
[Answers and Votes](/assets/gcp/discussion/70.ans.html)  


# 71

Your company is running a stateless application on a Compute Engine instance. The application is used heavily during regular business hours and lightly outside of business hours. Users are reporting that the application is slow during peak hours. You need to optimize the application's performance. What should you do?        

A. Create a snapshot of the existing disk. Create an instance template from the snapshot. Create an autoscaled managed instance group from the instance template.  
B. Create a snapshot of the existing disk. Create a custom image from the snapshot. Create an autoscaled managed instance group from the custom image.  
C. Create a custom image from the existing disk. Create an instance template from the custom image. Create an autoscaled managed instance group from the instance template.  
D. Create an instance template from the existing disk. Create a custom image from the instance template. Create an autoscaled managed instance group from the custom image.    

[Discussion](/assets/gcp/discussion/71.md)  
[Answers and Votes](/assets/gcp/discussion/71.ans.html)  


# 72

Your web application has several VM instances running within a VPC. You want to restrict communications between instances to only the paths and ports you authorize, but you don't want to rely on static IP addresses or subnets because the app can autoscale. How should you restrict communications?        

A. Use separate VPCs to restrict traffic  

B. Use firewall rules based on network tags attached to the compute instances  

C. Use Cloud DNS and only allow connections from authorized hostnames  

D. Use service accounts and configure the web application to authorize particular service accounts to have access    

[Discussion](/assets/gcp/discussion/72.md)  
[Answers and Votes](/assets/gcp/discussion/72.ans.html)  


# 73

You are using Cloud SQL as the database backend for a large CRM deployment. You want to scale as usage increases and ensure that you don't run out of storage, maintain 75% CPU usage cores, and keep replication lag below 60 seconds. What are the correct steps to meet your requirements?        
  
A. 1. Enable automatic storage increase for the instance. 2. Create a Stackdriver alert when CPU usage exceeds 75%, and change the instance type to reduce CPU usage. 3. Create a Stackdriver alert for replication lag, and shard the database to reduce replication time.  

B. 1. Enable automatic storage increase for the instance. 2. Change the instance type to a 32-core machine type to keep CPU usage below 75%. 3. Create a Stackdriver alert for replication lag, and deploy memcache to reduce load on the master.  

C. 1. Create a Stackdriver alert when storage exceeds 75%, and increase the available storage on the instance to create more space. 2. Deploy memcached to reduce CPU load. 3. Change the instance type to a 32-core machine type to reduce replication lag.  

D. 1. Create a Stackdriver alert when storage exceeds 75%, and increase the available storage on the instance to create more space. 2. Deploy memcached to reduce CPU load. 3. Create a Stackdriver alert for replication lag, and change the instance type to a 32-core machine type to reduce replication lag.    

[Discussion](/assets/gcp/discussion/73.md)  
[Answers and Votes](/assets/gcp/discussion/73.ans.html)  


# 74

You are tasked with building an online analytical processing (OLAP) marketing analytics and reporting tool. This requires a relational database that can operate on hundreds of terabytes of data. What is the Google-recommended tool for such applications?        

A. Cloud Spanner, because it is globally distributed  

B. Cloud SQL, because it is a fully managed relational database  

C. Cloud Firestore, because it offers real-time synchronization across devices  

D. BigQuery, because it is designed for large-scale processing of tabular data    


[Discussion](/assets/gcp/discussion/74.md)  
[Answers and Votes](/assets/gcp/discussion/74.ans.html)  


# 75
You have deployed an application to Google Kubernetes Engine (GKE), and are using the Cloud SQL proxy container to make the Cloud SQL database available to the services running on Kubernetes. You are notified that the application is reporting database connection issues. Your company policies require a post- mortem. What should you do?        

A. Use gcloud sql instances restart.  

B. Validate that the Service Account used by the Cloud SQL proxy container still has the Cloud Build Editor role.  

C. In the GCP Console, navigate to Stackdriver Logging. Consult logs for (GKE) and Cloud SQL.  

D. In the GCP Console, navigate to Cloud SQL. Restore the latest backup. Use kubectl to restart all pods.    

[Discussion](/assets/gcp/discussion/75.md)  
[Answers and Votes](/assets/gcp/discussion/75.ans.html)  


# 76
Your company pushes batches of sensitive transaction data from its application server VMs to Cloud Pub/Sub for processing and storage. What is the Google- recommended way for your application to authenticate to the required Google Cloud services?        


A. Ensure that VM service accounts are granted the appropriate Cloud Pub/Sub IAM roles.  

B. Ensure that VM service accounts do not have access to Cloud Pub/Sub, and use VM access scopes to grant the appropriate Cloud Pub/Sub IAM roles.  

C. Generate an OAuth2 access token for accessing Cloud Pub/Sub, encrypt it, and store it in Cloud Storage for access from each VM.  

D. Create a gateway to Cloud Pub/Sub using a Cloud Function, and grant the Cloud Function service account the appropriate Cloud Pub/Sub IAM roles.    

[Discussion](/assets/gcp/discussion/76.md)  
[Answers and Votes](/assets/gcp/discussion/76.ans.html)  


# 77

You want to establish a Compute Engine application in a single VPC across two regions. The application must communicate over VPN to an on-premises network.
How should you deploy the VPN?        


A. Use VPC Network Peering between the VPC and the on-premises network.  

B. Expose the VPC to the on-premises network using IAM and VPC Sharing.  

C. Create a global Cloud VPN Gateway with VPN tunnels from each region to the on-premises peer gateway.  

D. Deploy Cloud VPN Gateway in each region. Ensure that each region has at least one VPN tunnel to the on-premises peer gateway.    

[Discussion](/assets/gcp/discussion/77.md)  
[Answers and Votes](/assets/gcp/discussion/77.ans.html)  

# 78

Your applications will be writing their logs to BigQuery for analysis. Each application should have its own table. Any logs older than 45 days should be removed.
You want to optimize storage and follow Google-recommended practices. What should you do?        


A. Configure the expiration time for your tables at 45 days  

B. Make the tables time-partitioned, and configure the partition expiration at 45 days  

C. Rely on BigQuery's default behavior to prune application logs older than 45 days  

D. Create a script that uses the BigQuery command line tool (bq) to remove records older than 45 days    

[Discussion](/assets/gcp/discussion/78.md)  
[Answers and Votes](/assets/gcp/discussion/78.ans.html)  


# 79

You want your Google Kubernetes Engine cluster to automatically add or remove nodes based on CPU load.  
What should you do?        


A. Configure a HorizontalPodAutoscaler with a target CPU usage. Enable the Cluster Autoscaler from the GCP Console.  
B. Configure a HorizontalPodAutoscaler with a target CPU usage. Enable autoscaling on the managed instance group for the cluster using the gcloud command.  
C. Create a deployment and set the maxUnavailable and maxSurge properties. Enable the Cluster Autoscaler using the gcloud command.  
D. Create a deployment and set the maxUnavailable and maxSurge properties. Enable autoscaling on the cluster managed instance group from the GCP Console.    

[Discussion](/assets/gcp/discussion/79.md)  
[Answers and Votes](/assets/gcp/discussion/79.ans.html)  


# 80

You need to develop procedures to verify resilience of disaster recovery for remote recovery using GCP. Your production environment is hosted on-premises. You need to establish a secure, redundant connection between your on-premises network and the GCP network.  
What should you do?        


A. Verify that Dedicated Interconnect can replicate files to GCP. Verify that direct peering can establish a secure connection between your networks if Dedicated Interconnect fails.  

B. Verify that Dedicated Interconnect can replicate files to GCP. Verify that Cloud VPN can establish a secure connection between your networks if Dedicated Interconnect fails.  

C. Verify that the Transfer Appliance can replicate files to GCP. Verify that direct peering can establish a secure connection between your networks if the Transfer Appliance fails.  

D. Verify that the Transfer Appliance can replicate files to GCP. Verify that Cloud VPN can establish a secure connection between your networks if the Transfer Appliance fails.    


[Discussion](/assets/gcp/discussion/80.md)  
[Answers and Votes](/assets/gcp/discussion/80.ans.html)  


# 81

Your company operates nationally and plans to use GCP for multiple batch workloads, including some that are not time-critical. You also need to use GCP services that are HIPAA-certified and manage service costs.  
How should you design to meet Google best practices?        
    

A. Provision preemptible VMs to reduce cost. Discontinue use of all GCP services and APIs that are not HIPAA-compliant.  
B. Provision preemptible VMs to reduce cost. Disable and then discontinue use of all GCP services and APIs that are not HIPAA-compliant.  
C. Provision standard VMs in the same region to reduce cost. Discontinue use of all GCP services and APIs that are not HIPAA-compliant.  
D. Provision standard VMs to the same region to reduce cost. Disable and then discontinue use of all GCP services and APIs that are not HIPAA-compliant.    

[Discussion](/assets/gcp/discussion/81.md)  
[Answers and Votes](/assets/gcp/discussion/81.ans.html)  

# 82

Your customer wants to do resilience testing of their authentication layer. This consists of a regional managed instance group serving a public REST API that reads from and writes to a Cloud SQL instance.  
What should you do?        
您的客户想要对其身份验证层进行弹性测试。该层包含一个区域托管实例组，该实例组提供公共 REST API，用于读取和写入 Cloud SQL 实例。  
您应该怎么做？    

A. Engage with a security company to run web scrapers that look your for users' authentication data om malicious websites and notify you if any is found.  
B. Deploy intrusion detection software to your virtual machines to detect and log unauthorized access.  
C. Schedule a disaster simulation exercise during which you can shut off all VMs in a zone to see how your application behaves.  
D. Configure a read replica for your Cloud SQL instance in a different zone than the master, and then manually trigger a failover while monitoring KPIs for our REST API.    

[Discussion](/assets/gcp/discussion/82.md)  
[Answers and Votes](/assets/gcp/discussion/82.ans.html)  


# 83

Your BigQuery project has several users. For audit purposes, you need to see how many queries each user ran in the last month. What should you do?        
您的 BigQuery 项目有多个用户。为了进行审核，您需要查看每个用户上个月运行了多少次查询。您应该怎么做？    

A. Connect Google Data Studio to BigQuery. Create a dimension for the users and a metric for the amount of queries per user.  
B. In the BigQuery interface, execute a query on the JOBS table to get the required information.  
C. Use 'bq show' to list all jobs. Per job, use 'bq ls' to list job information and get the required information.  
D. Use Cloud Audit Logging to view Cloud Audit Logs, and create a filter on the query operation to get the required information.    

[Discussion](/assets/gcp/discussion/83.md)  
[Answers and Votes](/assets/gcp/discussion/83.ans.html)  


# 84

You want to automate the creation of a managed instance group. The VMs have many OS package dependencies. You want to minimize the startup time for new
VMs in the instance group.  
What should you do?         

A. Use Terraform to create the managed instance group and a startup script to install the OS package dependencies.  
B. Create a custom VM image with all OS package dependencies. Use Deployment Manager to create the managed instance group with the VM image.  
C. Use Puppet to create the managed instance group and install the OS package dependencies.  
D. Use Deployment Manager to create the managed instance group and Ansible to install the OS package dependencies.    

[Discussion](/assets/gcp/discussion/84.md)  
[Answers and Votes](/assets/gcp/discussion/84.ans.html)  


# 85

Your company captures all web traffic data in Google Analytics 360 and stores it in BigQuery. Each country has its own dataset. Each dataset has multiple tables.
You want analysts from each country to be able to see and query only the data for their respective countries.  
How should you configure the access rights?        
  

A. Create a group per country. Add analysts to their respective country-groups. Create a single group 'all_analysts', and add all country-groups as members. Grant the 'all_analysts' group the IAM role of BigQuery jobUser. Share the appropriate dataset with view access with each respective analyst country-group.  

B. Create a group per country. Add analysts to their respective country-groups. Create a single group 'all_analysts', and add all country-groups as members. Grant the 'all_analysts' group the IAM role of BigQuery jobUser. Share the appropriate tables with view access with each respective analyst country-group.  

C. Create a group per country. Add analysts to their respective country-groups. Create a single group 'all_analysts', and add all country-groups as members. Grant the 'all_analysts' group the IAM role of BigQuery dataViewer. Share the appropriate dataset with view access with each respective analyst country- group.  

D. Create a group per country. Add analysts to their respective country-groups. Create a single group 'all_analysts', and add all country-groups as members. Grant the 'all_analysts' group the IAM role of BigQuery dataViewer. Share the appropriate table with view access with each respective analyst country-group.    

[Discussion](/assets/gcp/discussion/85.md)  
[Answers and Votes](/assets/gcp/discussion/85.ans.html)  

# 86

You have been engaged by your client to lead the migration of their application infrastructure to GCP. One of their current problems is that the on-premises high performance SAN is requiring frequent and expensive upgrades to keep up with the variety of workloads that are identified as follows: 20 TB of log archives retained for legal reasons; 500 GB of VM boot/data volumes and templates; 500 GB of image thumbnails; 200 GB of customer session state data that allows customers to restart sessions even if off-line for several days.  
Which of the following best reflects your recommendations for a cost-effective storage allocation?          
   

A. Local SSD for customer session state data. Lifecycle-managed Cloud Storage for log archives, thumbnails, and VM boot/data volumes.  
B. Memcache backed by Cloud Datastore for the customer session state data. Lifecycle-managed Cloud Storage for log archives, thumbnails, and VM boot/data volumes.  
C. Memcache backed by Cloud SQL for customer session state data. Assorted local SSD-backed instances for VM boot/data volumes. Cloud Storage for log archives and thumbnails.  
D. Memcache backed by Persistent Disk SSD storage for customer session state data. Assorted local SSD-backed instances for VM boot/data volumes. Cloud Storage for log archives and thumbnails.    

[Discussion](/assets/gcp/discussion/86.md)    
[Answers and Votes](/assets/gcp/discussion/86.ans.html)  


# 87

Your web application uses Google Kubernetes Engine to manage several workloads. One workload requires a consistent set of hostnames even after pod scaling and relaunches.  
Which feature of Kubernetes should you use to accomplish this?             

A. StatefulSets  
B. Role-based access control  
C. Container environment variables  
D. Persistent Volumes    

[Discussion](/assets/gcp/discussion/87.md)  

# 88

You are using Cloud CDN to deliver static HTTP(S) website content hosted on a Compute Engine instance group. You want to improve the cache hit ratio.
What should you do?          

A. Customize the cache keys to omit the protocol from the key.  
B. Shorten the expiration time of the cached objects.  
C. Make sure the HTTP(S) header ג€Cache-Regionג€ points to the closest region of your users.  
D. Replicate the static content in a Cloud Storage bucket. Point CloudCDN toward a load balancer on that bucket.    

[Discussion](/assets/gcp/discussion/88.md)  
[Answers and Votes](/assets/gcp/discussion/88.ans.html)  


# 89

Your architecture calls for the centralized collection of all admin activity and VM system logs within your project.  
How should you collect these logs from both VMs and services?          

A. All admin and VM system logs are automatically collected by Stackdriver.  
B. Stackdriver automatically collects admin activity logs for most services. The Stackdriver Logging agent must be installed on each instance to collect system logs.  
C. Launch a custom syslogd compute instance and configure your GCP project and VMs to forward all logs to it.  
D. Install the Stackdriver Logging agent on a single compute instance and let it collect all audit and access logs for your environment.    

[Discussion](/assets/gcp/discussion/89.md)  
[Answers and Votes](/assets/gcp/discussion/89.ans.html)  


# 90
You have an App Engine application that needs to be updated. You want to test the update with production traffic before replacing the current application version.
What should you do?          

A. Deploy the update using the Instance Group Updater to create a partial rollout, which allows for canary testing.  
B. Deploy the update as a new version in the App Engine application, and split traffic between the new and current versions.  
C. Deploy the update in a new VPC, and use Google's global HTTP load balancing to split traffic between the update and current applications.  
D. Deploy the update as a new App Engine application, and use Google's global HTTP load balancing to split traffic between the new and current applications.    

[Discussion](/assets/gcp/discussion/90.md)  
[Answers and Votes](/assets/gcp/discussion/90.ans.html)  


# 91
All Compute Engine instances in your VPC should be able to connect to an Active Directory server on specific ports. Any other traffic emerging from your instances is not allowed. You want to enforce this using VPC firewall rules.
How should you configure the firewall rules?      
   

A. Create an egress rule with priority 1000 to deny all traffic for all instances. Create another egress rule with priority 100 to allow the Active Directory traffic for all instances.
B. Create an egress rule with priority 100 to deny all traffic for all instances. Create another egress rule with priority 1000 to allow the Active Directory traffic for all instances.
C. Create an egress rule with priority 1000 to allow the Active Directory traffic. Rely on the implied deny egress rule with priority 100 to block all traffic for all instances.
D. Create an egress rule with priority 100 to allow the Active Directory traffic. Rely on the implied deny egress rule with priority 1000 to block all traffic for all instances.  

[Discussion](/assets/gcp/discussion/91.md)  
[Answers and Votes](/assets/gcp/discussion/91.ans.html)  


# 92

Your customer runs a web service used by e-commerce sites to offer product recommendations to users. The company has begun experimenting with a machine learning model on Google Cloud Platform to improve the quality of results.
What should the customer do to improve their model's results over time?      
   

A. Export Cloud Machine Learning Engine performance metrics from Stackdriver to BigQuery, to be used to analyze the efficiency of the model.
B. Build a roadmap to move the machine learning model training from Cloud GPUs to Cloud TPUs, which offer better results.
C. Monitor Compute Engine announcements for availability of newer CPU architectures, and deploy the model to them as soon as they are available for additional performance.
D. Save a history of recommendations and results of the recommendations in BigQuery, to be used as training data.  

[Discussion](/assets/gcp/discussion/92.md)  
[Answers and Votes](/assets/gcp/discussion/92.ans.html)  


# 93

A development team at your company has created a dockerized HTTPS web application. You need to deploy the application on Google Kubernetes Engine (GKE) and make sure that the application scales automatically.
How should you deploy to GKE?      

A. Use the Horizontal Pod Autoscaler and enable cluster autoscaling. Use an Ingress resource to load-balance the HTTPS traffic.
B. Use the Horizontal Pod Autoscaler and enable cluster autoscaling on the Kubernetes cluster. Use a Service resource of type LoadBalancer to load-balance the HTTPS traffic.
C. Enable autoscaling on the Compute Engine instance group. Use an Ingress resource to load-balance the HTTPS traffic.
D. Enable autoscaling on the Compute Engine instance group. Use a Service resource of type LoadBalancer to load-balance the HTTPS traffic.  
    


[Discussion](/assets/gcp/discussion/93.md)  
[Answers and Votes](/assets/gcp/discussion/93.ans.html)  


# 94

You need to design a solution for global load balancing based on the URL path being requested. You need to ensure operations reliability and end-to-end in- transit encryption based on Google best practices.
What should you do?      

A. Create a cross-region load balancer with URL Maps.
B. Create an HTTPS load balancer with URL Maps.
C. Create appropriate instance groups and instances. Configure SSL proxy load balancing.
D. Create a global forwarding rule. Configure SSL proxy load balancing.  

[Discussion](/assets/gcp/discussion/94.md)  
[Answers and Votes](/assets/gcp/discussion/94.ans.html)  


# 95

You have an application that makes HTTP requests to Cloud Storage. Occasionally the requests fail with HTTP status codes of 5xx and 429.  
How should you handle these types of errors?        
  

A. Use gRPC instead of HTTP for better performance.  
B. Implement retry logic using a truncated exponential backoff strategy.  
C. Make sure the Cloud Storage bucket is multi-regional for geo-redundancy.  
D. Monitor https://status.cloud.google.com/feed.atom and only make requests if Cloud Storage is not reporting an incident.    

[Discussion](/assets/gcp/discussion/95.md)  
[Answers and Votes](/assets/gcp/discussion/95.ans.html)  


# 96

You need to develop procedures to test a disaster plan for a mission-critical application. You want to use Google-recommended practices and native capabilities within GCP.  
What should you do?        
 

A. Use Deployment Manager to automate service provisioning. Use Activity Logs to monitor and debug your tests.  
B. Use Deployment Manager to automate service provisioning. Use Stackdriver to monitor and debug your tests.  
C. Use gcloud scripts to automate service provisioning. Use Activity Logs to monitor and debug your tests.  
D. Use gcloud scripts to automate service provisioning. Use Stackdriver to monitor and debug your tests.    

[Discussion](/assets/gcp/discussion/96.md)  
[Answers and Votes](/assets/gcp/discussion/96.ans.html)  


# 97

Your company creates rendering software which users can download from the company website. Your company has customers all over the world. You want to minimize latency for all your customers. You want to follow Google-recommended practices.  
How should you store the files?        
 

A. Save the files in a Multi-Regional Cloud Storage bucket.  
B. Save the files in a Regional Cloud Storage bucket, one bucket per zone of the region.  
C. Save the files in multiple Regional Cloud Storage buckets, one bucket per zone per region.  
D. Save the files in multiple Multi-Regional Cloud Storage buckets, one bucket per multi-region.    

[Discussion](/assets/gcp/discussion/97.md)  
[Answers and Votes](/assets/gcp/discussion/97.ans.html)  


# 98

Your company acquired a healthcare startup and must retain its customers' medical information for up to 4 more years, depending on when it was created. Your corporate policy is to securely retain this data, and then delete it as soon as regulations allow.  
Which approach should you take?        


A. Store the data in Google Drive and manually delete records as they expire.  
B. Anonymize the data using the Cloud Data Loss Prevention API and store it indefinitely.  
C. Store the data in Cloud Storage and use lifecycle management to delete files when they expire.  
D. Store the data in Cloud Storage and run a nightly batch script that deletes all expired data.    

[Discussion](/assets/gcp/discussion/98.md)  
[Answers and Votes](/assets/gcp/discussion/98.ans.html)  


# 99

You are deploying a PHP App Engine Standard service with Cloud SQL as the backend. You want to minimize the number of queries to the database.
What should you do?        
   

A. Set the memcache service level to dedicated. Create a key from the hash of the query, and return database values from memcache before issuing a query to Cloud SQL.  
B. Set the memcache service level to dedicated. Create a cron task that runs every minute to populate the cache with keys containing query results.  
C. Set the memcache service level to shared. Create a cron task that runs every minute to save all expected queries to a key called ג€cached_queriesג€.  
D. Set the memcache service level to shared. Create a key called ג€cached_queriesג€, and return database values from the key before using a query to Cloud SQL.    

[Discussion](/assets/gcp/discussion/99.md)  
[Answers and Votes](/assets/gcp/discussion/99.ans.html)  


# 100

You need to ensure reliability for your application and operations by supporting reliable task scheduling for compute on GCP. Leveraging Google best practices, what should you do?        


A. Using the Cron service provided by App Engine, publish messages directly to a message-processing utility service running on Compute Engine instances.  
B. Using the Cron service provided by App Engine, publish messages to a Cloud Pub/Sub topic. Subscribe to that topic using a message-processing utility service running on Compute Engine instances.  
C. Using the Cron service provided by Google Kubernetes Engine (GKE), publish messages directly to a message-processing utility service running on Compute Engine instances.  
D. Using the Cron service provided by GKE, publish messages to a Cloud Pub/Sub topic. Subscribe to that topic using a message-processing utility service running on Compute Engine instances.    

[Discussion](/assets/gcp/discussion/100.md)