---
layout: home
title: "professional cloud architect 251-279"
date: 2025-04-11 12:00:00 +0800
lastupdated: 2025-04-11 12:00:00 +0800
categories: cloud
tags: [ai,k8s,cloud]
---
professional cloud architect 2025-04-11 12:00:00
  
# 251    

Introductory Info  
Company Overview -  
TerramEarth manufactures heavy equipment for the mining and agricultural industries. About 80% of their business is from mining and 20% from agriculture. They currently have over 500 dealers and service centers in 100 countries. Their mission is to build products that make their customers more productive.    

Solution Concept -    
There are 20 million TerramEarth vehicles in operation that collect 120 fields of data per second. Data is stored locally on the vehicle and can be accessed for analysis when a vehicle is serviced. The data is downloaded via a maintenance port. This same port can be used to adjust operational parameters, allowing the vehicles to be upgraded in the field with new computing modules.  
Approximately 200,000 vehicles are connected to a cellular network, allowing TerramEarth to collect data directly. At a rate of 120 fields of data per second, with
22 hours of operation per day, TerramEarth collects a total of about 9 TB/day from these connected vehicles.    

Existing Technical Environment -  
TerramEarth's existing architecture is composed of Linux and Windows-based systems that reside in a single U.S, west coast based data center. These systems gzip CSV files from the field and upload via FTP, and place the data in their data warehouse. Because this process takes time, aggregated reports are based on data that is 3 weeks old.  
With this data, TerramEarth has been able to preemptively stock replacement parts and reduce unplanned downtime of their vehicles by 60%. However, because the data is stale, some customers are without their vehicles for up to 4 weeks while they wait for replacement parts.    

Business Requirements -  
Decrease unplanned vehicle downtime to less than 1 week  
Support the dealer network with more data on how their customers use their equipment to better position new products and services  
Have the ability to partner with different companies `" especially with seed and fertilizer suppliers in the fast-growing agricultural business `" to create compelling joint offerings for their customers    

Technical Requirements -  
Expand beyond a single datacenter to decrease latency to the American midwest and east coast  
Create a backup strategy  
Increase security of data transfer from equipment to the datacenter  
Improve data in the data warehouse  
Use customer and equipment data to anticipate customer needs    

Application 1: Data ingest -  
A custom Python application reads uploaded datafiles from a single server, writes to the data warehouse.  
Compute:  
Windows Server 2008 R2    
- 16 CPUs    
- 128 GB of RAM    
- 10 TB local HDD storage    

Application 2: Reporting -  
An off the shelf application that business analysts use to run a daily report to see what equipment needs repair. Only 2 analysts of a team of 10 (5 west coast, 5 east coast) can connect to the reporting application at a time.  
Compute:  
Off the shelf application. License tied to number of physical CPUs    
- Windows Server 2008 R2    
- 16 CPUs    
- 32 GB of RAM    
- 500 GB HDD  
Data warehouse:  
A single PostgreSQL server    
- RedHat Linux    
- 64 CPUs      
- 128 GB of RAM    
- 4x 6TB HDD in RAID 0    

Executive Statement -  
Our competitive advantage has always been in our manufacturing process, with our ability to build better vehicles for lower cost than our competitors. However, new products with different approaches are constantly being developed, and I'm concerned that we lack the skills to undergo the next wave of transformations in our industry. My goals are to build our skills while addressing immediate market needs through incremental innovations.  
Question  
For this question, refer to the TerramEarth case study. To be compliant with European GDPR regulation, TerramEarth is required to delete data generated from its
European customers after a period of 36 months when it contains personal data. In the new architecture, this data will be stored in both Cloud Storage and
BigQuery. What should you do?          

A. Create a BigQuery table for the European data, and set the table retention period to 36 months. For Cloud Storage, use gsutil to enable lifecycle management using a DELETE action with an Age condition of 36 months.  
B. Create a BigQuery table for the European data, and set the table retention period to 36 months. For Cloud Storage, use gsutil to create a SetStorageClass to NONE action when with an Age condition of 36 months.  
C. Create a BigQuery time-partitioned table for the European data, and set the partition expiration period to 36 months. For Cloud Storage, use gsutil to enable lifecycle management using a DELETE action with an Age condition of 36 months.  
D. Create a BigQuery time-partitioned table for the European data, and set the partition expiration period to 36 months. For Cloud Storage, use gsutil to create a SetStorageClass to NONE action with an Age condition of 36 months.    
  
[Discussion](/assets/gcp/discussion/251.md)  
[Answers and Votes](/assets/gcp/discussion/251.ans.html)  
  
# 252    

Question  
For this question, refer to the TerramEarth case study. TerramEarth has decided to store data files in Cloud Storage. You need to configure Cloud Storage lifecycle rule to store 1 year of data and minimize file storage cost.  
Which two actions should you take?          

A. Create a Cloud Storage lifecycle rule with Age: ג€30ג€, Storage Class: ג€Standardג€, and Action: ג€Set to Coldlineג€, and create a second GCS life-cycle rule with Age: ג€365ג€, Storage Class: ג€Coldlineג€, and Action: ג€Deleteג€.  
B. Create a Cloud Storage lifecycle rule with Age: ג€30ג€, Storage Class: ג€Coldlineג€, and Action: ג€Set to Nearlineג€, and create a second GCS life-cycle rule with Age: ג€91ג€, Storage Class: ג€Coldlineג€, and Action: ג€Set to Nearlineג€.  
C. Create a Cloud Storage lifecycle rule with Age: ג€90ג€, Storage Class: ג€Standardג€, and Action: ג€Set to Nearlineג€, and create a second GCS life-cycle rule with Age: ג€91ג€, Storage Class: ג€Nearlineג€, and Action: ג€Set to Coldlineג€.  
D. Create a Cloud Storage lifecycle rule with Age: ג€30ג€, Storage Class: ג€Standardג€, and Action: ג€Set to Coldlineג€, and create a second GCS life-cycle rule with Age: ג€365ג€, Storage Class: ג€Nearlineג€, and Action: ג€Deleteג€.    
  
[Discussion](/assets/gcp/discussion/252.md)  
[Answers and Votes](/assets/gcp/discussion/252.ans.html)  

  
# 253    

Question  
For this question, refer to the TerramEarth case study. You need to implement a reliable, scalable GCP solution for the data warehouse for your company,  
TerramEarth.  
Considering the TerramEarth business and technical requirements, what should you do?          

A. Replace the existing data warehouse with BigQuery. Use table partitioning.  
B. Replace the existing data warehouse with a Compute Engine instance with 96 CPUs.  
C. Replace the existing data warehouse with BigQuery. Use federated data sources.  
D. Replace the existing data warehouse with a Compute Engine instance with 96 CPUs. Add an additional Compute Engine preemptible instance with 32 CPUs.    
  
[Discussion](/assets/gcp/discussion/253.md)  
[Answers and Votes](/assets/gcp/discussion/253.ans.html)  

  
# 254    

Question  
For this question, refer to the TerramEarth case study. A new architecture that writes all incoming data to BigQuery has been introduced. You notice that the data is dirty, and want to ensure data quality on an automated daily basis while managing cost.  
What should you do?          

A. Set up a streaming Cloud Dataflow job, receiving data by the ingestion process. Clean the data in a Cloud Dataflow pipeline.  
B. Create a Cloud Function that reads data from BigQuery and cleans it. Trigger the Cloud Function from a Compute Engine instance.  
C. Create a SQL statement on the data in BigQuery, and save it as a view. Run the view daily, and save the result to a new table.  
D. Use Cloud Dataprep and configure the BigQuery tables as the source. Schedule a daily job to clean the data.    
  
[Discussion](/assets/gcp/discussion/254.md)  
[Answers and Votes](/assets/gcp/discussion/254.ans.html)  

  
# 255    

Question  
For this question, refer to the TerramEarth case study. Considering the technical requirements, how should you reduce the unplanned vehicle downtime in GCP?          
  
A. Use BigQuery as the data warehouse. Connect all vehicles to the network and stream data into BigQuery using Cloud Pub/Sub and Cloud Dataflow. Use Google Data Studio for analysis and reporting.  
B. Use BigQuery as the data warehouse. Connect all vehicles to the network and upload gzip files to a Multi-Regional Cloud Storage bucket using gcloud. Use Google Data Studio for analysis and reporting.  
C. Use Cloud Dataproc Hive as the data warehouse. Upload gzip files to a Multi-Regional Cloud Storage bucket. Upload this data into BigQuery using gcloud. Use Google Data Studio for analysis and reporting.  
D. Use Cloud Dataproc Hive as the data warehouse. Directly stream data into partitioned Hive tables. Use Pig scripts to analyze data.    
    
[Discussion](/assets/gcp/discussion/255.md)    
[Answers and Votes](/assets/gcp/discussion/255.ans.html)  

  
# 256    

Question
For this question, refer to the TerramEarth case study. You are asked to design a new architecture for the ingestion of the data of the 200,000 vehicles that are connected to a cellular network. You want to follow Google-recommended practices.  
Considering the technical requirements, which components should you use for the ingestion of the data?          

A. Google Kubernetes Engine with an SSL Ingress  
B. Cloud IoT Core with public/private key pairs  
C. Compute Engine with project-wide SSH keys  
D. Compute Engine with specific SSH keys    
  
[Discussion](/assets/gcp/discussion/256.md)  
[Answers and Votes](/assets/gcp/discussion/256.ans.html)  

  
# 257    

Question  
For this question, refer to the TerramEarth case study. You start to build a new application that uses a few Cloud Functions for the backend. One use case requires a Cloud Function func_display to invoke another Cloud Function func_query. You want func_query only to accept invocations from func_display. You also want to follow Google's recommended best practices. What should you do?          

A. Create a token and pass it in as an environment variable to func_display. When invoking func_query, include the token in the request. Pass the same token to func_query and reject the invocation if the tokens are different.  
B. Make func_query 'Require authentication.' Create a unique service account and associate it to func_display. Grant the service account invoker role for func_query. Create an id token in func_display and include the token to the request when invoking func_query.  
C. Make func_query 'Require authentication' and only accept internal traffic. Create those two functions in the same VPC. Create an ingress firewall rule for func_query to only allow traffic from func_display.  
D. Create those two functions in the same project and VPC. Make func_query only accept internal traffic. Create an ingress firewall for func_query to only allow traffic from func_display. Also, make sure both functions use the same service account.     
  
[Discussion](/assets/gcp/discussion/257.md)  
[Answers and Votes](/assets/gcp/discussion/257.ans.html)  

  
# 258    

Question  
For this question, refer to the TerramEarth case study. You have broken down a legacy monolithic application into a few containerized RESTful microservices.  
You want to run those microservices on Cloud Run. You also want to make sure the services are highly available with low latency to your customers. What should you do?          

A. Deploy Cloud Run services to multiple availability zones. Create Cloud Endpoints that point to the services. Create a global HTTP(S) Load Balancing instance and attach the Cloud Endpoints to its backend.  
B. Deploy Cloud Run services to multiple regions. Create serverless network endpoint groups pointing to the services. Add the serverless NEGs to a backend service that is used by a global HTTP(S) Load Balancing instance.  
C. Deploy Cloud Run services to multiple regions. In Cloud DNS, create a latency-based DNS name that points to the services.  
D. Deploy Cloud Run services to multiple availability zones. Create a TCP/IP global load balancer. Add the Cloud Run Endpoints to its backend service.    
  
[Discussion](/assets/gcp/discussion/258.md)  
[Answers and Votes](/assets/gcp/discussion/258.ans.html)  

  
# 259    

Question  
For this question, refer to the TerramEarth case study. You are migrating a Linux-based application from your private data center to Google Cloud. The
TerramEarth security team sent you several recent Linux vulnerabilities published by Common Vulnerabilities and Exposures (CVE). You need assistance in understanding how these vulnerabilities could impact your migration. What should you do?       (Choose two.)    

A. Open a support case regarding the CVE and chat with the support engineer.  
B. Read the CVEs from the Google Cloud Status Dashboard to understand the impact.  
C. Read the CVEs from the Google Cloud Platform Security Bulletins to understand the impact.  
D. Post a question regarding the CVE in Stack Overflow to get an explanation.  
E. Post a question regarding the CVE in a Google Cloud discussion group to get an explanation.    
  
[Discussion](/assets/gcp/discussion/259.md)  
[Answers and Votes](/assets/gcp/discussion/259.ans.html)  

  
# 260    

Question  
For this question, refer to the TerramEarth case study. TerramEarth has a legacy web application that you cannot migrate to cloud. However, you still want to build a cloud-native way to monitor the application. If the application goes down, you want the URL to point to a "Site is unavailable" page as soon as possible. You also want your Ops team to receive a notification for the issue. You need to build a reliable solution for minimum cost. What should you do?          

A. Create a scheduled job in Cloud Run to invoke a container every minute. The container will check the application URL. If the application is down, switch the URL to the "Site is unavailable" page, and notify the Ops team.  
B. Create a cron job on a Compute Engine VM that runs every minute. The cron job invokes a Python program to check the application URL. If the application is down, switch the URL to the "Site is unavailable" page, and notify the Ops team.  
C. Create a Cloud Monitoring uptime check to validate the application URL. If it fails, put a message in a Pub/Sub queue that triggers a Cloud Function to switch the URL to the "Site is unavailable" page, and notify the Ops team.  
D. Use Cloud Error Reporting to check the application URL. If the application is down, switch the URL to the "Site is unavailable" page, and notify the Ops team.    
  
[Discussion](/assets/gcp/discussion/260.md)  
[Answers and Votes](/assets/gcp/discussion/260.ans.html)  

  
# 261    

Question  
For this question, refer to the TerramEarth case study. You are building a microservice-based application for TerramEarth. The application is based on Docker containers. You want to follow Google-recommended practices to build the application continuously and store the build artifacts. What should you do?          

A. Configure a trigger in Cloud Build for new source changes. Invoke Cloud Build to build container images for each microservice, and tag them using the code commit hash. Push the images to the Container Registry.  
B. Configure a trigger in Cloud Build for new source changes. The trigger invokes build jobs and build container images for the microservices. Tag the images with a version number, and push them to Cloud Storage.  
C. Create a Scheduler job to check the repo every minute. For any new change, invoke Cloud Build to build container images for the microservices. Tag the images using the current timestamp, and push them to the Container Registry.  
D. Configure a trigger in Cloud Build for new source changes. Invoke Cloud Build to build one container image, and tag the image with the label 'latest.' Push the image to the Container Registry.    
  
[Discussion](/assets/gcp/discussion/261.md)  
[Answers and Votes](/assets/gcp/discussion/261.ans.html)  

  
# 262    

Question  
For this question, refer to the TerramEarth case study. TerramEarth has about 1 petabyte (PB) of vehicle testing data in a private data center. You want to move the data to Cloud Storage for your machine learning team. Currently, a 1-Gbps interconnect link is available for you. The machine learning team wants to start using the data in a month. What should you do?          

A. Request Transfer Appliances from Google Cloud, export the data to appliances, and return the appliances to Google Cloud. Most Voted  
B. Configure the Storage Transfer service from Google Cloud to send the data from your data center to Cloud Storage.  
C. Make sure there are no other users consuming the 1Gbps link, and use multi-thread transfer to upload the data to Cloud Storage.  
D. Export files to an encrypted USB device, send the device to Google Cloud, and request an import of the data to Cloud Storage.    
  
[Discussion](/assets/gcp/discussion/262.md)  
[Answers and Votes](/assets/gcp/discussion/262.ans.html)  

  
# 263    
  

Introductory Info  
Company Overview -  
Dress4Win is a web-based company that helps their users organize and manage their personal wardrobe using a website and mobile application. The company also cultivates an active social network that connects their users with designers and retailers. They monetize their services through advertising, e-commerce, referrals, and a premium app model.    

Company Background -  
Dress4Win's application has grown from a few servers in the founder's garage to several hundred servers and appliances in a collocated data center. However, the capacity of their infrastructure is now insufficient for the application's rapid growth. Because of this growth and the company's desire to innovate faster,  
Dress4Win is committing to a full migration to a public cloud.    

Solution Concept -  
For the first phase of their migration to the cloud, Dress4Win is considering moving their development and test environments. They are also considering building a disaster recovery site, because their current infrastructure is at a single location. They are not sure which components of their architecture they can migrate as is and which components they need to change before migrating them.    

Existing Technical Environment -  
The Dress4Win application is served out of a single data center location.  
Databases:    
- MySQL - user data, inventory, static data    
- Redis - metadata, social graph, caching  
Application servers:    
- Tomcat - Java micro-services    
- Nginx - static content    
- Apache Beam - Batch processing  
Storage appliances:    
- iSCSI for VM hosts    
- Fiber channel SAN - MySQL databases    
- NAS - image storage, logs, backups  
Apache Hadoop/Spark servers:    
- Data analysis    
- Real-time trending calculations  
MQ servers:    
- Messaging    
- Social notifications    
- Events  
Miscellaneous servers:    
- Jenkins, monitoring, bastion hosts, security scanners    

Business Requirements -  
Build a reliable and reproducible environment with scaled parity of production.    

Improve security by defining and adhering to a set of security and Identity and Access Management (IAM) best practices for cloud.  
Improve business agility and speed of innovation through rapid provisioning of new resources.  
Analyze and optimize architecture for performance in the cloud.  
Migrate fully to the cloud if all other requirements are met.    

Technical Requirements -  
Evaluate and choose an automation framework for provisioning resources in cloud.  
Support failover of the production environment to cloud during an emergency.  
Identify production services that can migrate to cloud to save capacity.  
Use managed services whenever possible.  
Encrypt data on the wire and at rest.  
Support multiple VPN connections between the production data center and cloud environment.    

CEO Statement -  
Our investors are concerned about our ability to scale and contain costs with our current infrastructure. They are also concerned that a new competitor could use a public cloud platform to offset their up-front investment and freeing them to focus on developing better features.    

CTO Statement -  
We have invested heavily in the current infrastructure, but much of the equipment is approaching the end of its useful life. We are consistently waiting weeks for new gear to be racked before we can start new projects. Our traffic patterns are highest in the mornings and weekend evenings; during other times, 80% of our capacity is sitting idle.    

CFO Statement -  
Our capital expenditure is now exceeding our quarterly projections. Migrating to the cloud will likely cause an initial increase in spending, but we expect to fully transition before our next hardware refresh cycle. Our total cost of ownership (TCO) analysis over the next 5 years puts a cloud strategy between 30 to 50% lower than our current model.    

Question  
The Dress4Win security team has disabled external SSH access into production virtual machines (VMs) on Google Cloud Platform (GCP).  
The operations team needs to remotely manage the VMs, build and push Docker containers, and manage Google Cloud Storage objects.  
What can they do?          

A. Grant the operations engineer access to use Google Cloud Shell.  
B. Configure a VPN connection to GCP to allow SSH access to the cloud VMs.  
C. Develop a new access request process that grants temporary SSH access to cloud VMs when an operations engineer needs to perform a task.  
D. Have the development team build an API service that allows the operations team to execute specific remote procedure calls to accomplish their tasks.    
  
[Discussion](/assets/gcp/discussion/263.md)  
[Answers and Votes](/assets/gcp/discussion/263.ans.html)  

  
# 264    

Question  
At Dress4Win, an operations engineer wants to create a tow-cost solution to remotely archive copies of database backup files.  
The database files are compressed tar files stored in their current data center.
How should he proceed?          

A. Create a cron script using gsutil to copy the files to a Coldline Storage bucket.  
B. Create a cron script using gsutil to copy the files to a Regional Storage bucket.  
C. Create a Cloud Storage Transfer Service Job to copy the files to a Coldline Storage bucket.  
D. Create a Cloud Storage Transfer Service job to copy the files to a Regional Storage bucket.    
  
  
[Discussion](/assets/gcp/discussion/264.md)  
[Answers and Votes](/assets/gcp/discussion/264.ans.html)  

  
# 265    

Question  
Dress4Win has asked you to recommend machine types they should deploy their application servers to.
How should you proceed?          

A. Perform a mapping of the on-premises physical hardware cores and RAM to the nearest machine types in the cloud.  
B. Recommend that Dress4Win deploy application servers to machine types that offer the highest RAM to CPU ratio available.  
C. Recommend that Dress4Win deploy into production with the smallest instances available, monitor them over time, and scale the machine type up until the desired performance is reached.  
D. Identify the number of virtual cores and RAM associated with the application server virtual machines align them to a custom machine type in the cloud, monitor performance, and scale the machine types up until the desired performance is reached.    
  
[Discussion](/assets/gcp/discussion/265.md)  
[Answers and Votes](/assets/gcp/discussion/265.ans.html)  

  
# 266    

Question  
As part of Dress4Win's plans to migrate to the cloud, they want to be able to set up a managed logging and monitoring system so they can handle spikes in their traffic load.  
They want to ensure that:    
* The infrastructure can be notified when it needs to scale up and down to handle the ebb and flow of usage throughout the day    
* Their administrators are notified automatically when their application reports errors.    
* They can filter their aggregated logs down in order to debug one piece of the application across many hosts  
Which Google StackDriver features should they use?          

A. Logging, Alerts, Insights, Debug  
B. Monitoring, Trace, Debug, Logging  
C. Monitoring, Logging, Alerts, Error Reporting  
D. Monitoring, Logging, Debug, Error Report    
  
[Discussion](/assets/gcp/discussion/266.md)  
[Answers and Votes](/assets/gcp/discussion/266.ans.html)  

  
# 267    

Question  
Dress4Win would like to become familiar with deploying applications to the cloud by successfully deploying some applications quickly, as is. They have asked for your recommendation.  
What should you advise?          

A. Identify self-contained applications with external dependencies as a first move to the cloud.  
B. Identify enterprise applications with internal dependencies and recommend these as a first move to the cloud.  
C. Suggest moving their in-house databases to the cloud and continue serving requests to on-premise applications.  
D. Recommend moving their message queuing servers to the cloud and continue handling requests to on-premise applications.    
  
[Discussion](/assets/gcp/discussion/267.md)  
[Answers and Votes](/assets/gcp/discussion/267.ans.html)  

  
# 268  
Question  
Dress4Win has asked you for advice on how to migrate their on-premises MySQL deployment to the cloud.  
They want to minimize downtime and performance impact to their on-premises solution during the migration.  
Which approach should you recommend?          

A. Create a dump of the on-premises MySQL master server, and then shut it down, upload it to the cloud environment, and load into a new MySQL cluster.  
B. Setup a MySQL replica server/slave in the cloud environment, and configure it for asynchronous replication from the MySQL master server on-premises until cutover.  
C. Create a new MySQL cluster in the cloud, configure applications to begin writing to both on premises and cloud MySQL masters, and destroy the original cluster at cutover.  
D. Create a dump of the MySQL replica server into the cloud environment, load it into: Google Cloud Datastore, and configure applications to read/write to Cloud Datastore at cutover.     
  
[Discussion](/assets/gcp/discussion/268.md)  
[Answers and Votes](/assets/gcp/discussion/268.ans.html)  

  
# 269    

Question  
Dress4Win has configured a new uptime check with Google Stackdriver for several of their legacy services. The Stackdriver dashboard is not reporting the services as healthy.  
What should they do?          

A. Install the Stackdriver agent on all of the legacy web servers.  
B. In the Cloud Platform Console download the list of the uptime servers' IP addresses and create an inbound firewall rule  
C. Configure their load balancer to pass through the User-Agent HTTP header when the value matches GoogleStackdriverMonitoring-UptimeChecks (https:// cloud.google.com/monitoring)  
D. Configure their legacy web servers to allow requests that contain user-Agent HTTP header when the value matches GoogleStackdriverMonitoring- UptimeChecks (https://cloud.google.com/monitoring)    
  
[Discussion](/assets/gcp/discussion/269.md)  
[Answers and Votes](/assets/gcp/discussion/269.ans.html)  

  
# 270    

Question  
As part of their new application experience, Dress4Wm allows customers to upload images of themselves.  
The customer has exclusive control over who may view these images.  
Customers should be able to upload images with minimal latency and also be shown their images quickly on the main application page when they log in.  
Which configuration should Dress4Win use?          

A. Store image files in a Google Cloud Storage bucket. Use Google Cloud Datastore to maintain metadata that maps each customer's ID and their image files.  
B. Store image files in a Google Cloud Storage bucket. Add custom metadata to the uploaded images in Cloud Storage that contains the customer's unique ID.  
C. Use a distributed file system to store customers' images. As storage needs increase, add more persistent disks and/or nodes. Assign each customer a unique ID, which sets each file's owner attribute, ensuring privacy of images.  
D. Use a distributed file system to store customers' images. As storage needs increase, add more persistent disks and/or nodes. Use a Google Cloud SQL database to maintain metadata that maps each customer's ID to their image files.    
  
[Discussion](/assets/gcp/discussion/270.md)  
[Answers and Votes](/assets/gcp/discussion/270.ans.html)  

  
# 271      

Question  
Dress4Win has end-to-end tests covering 100% of their endpoints.  
They want to ensure that the move to the cloud does not introduce any new bugs.  
Which additional testing methods should the developers employ to prevent an outage?          

A. They should enable Google Stackdriver Debugger on the application code to show errors in the code.  
B. They should add additional unit tests and production scale load tests on their cloud staging environment.  
C. They should run the end-to-end tests in the cloud staging environment to determine if the code is working as intended.  
D. They should add canary tests so developers can measure how much of an impact the new release causes to latency.    
  
[Discussion](/assets/gcp/discussion/271.md)  
[Answers and Votes](/assets/gcp/discussion/271.ans.html)  

  
# 272    

Question
You want to ensure Dress4Win's sales and tax records remain available for infrequent viewing by auditors for at least 10 years.  
Cost optimization is your top priority.  
Which cloud services should you choose?          

A. Google Cloud Storage Coldline to store the data, and gsutil to access the data.  
B. Google Cloud Storage Nearline to store the data, and gsutil to access the data.  
C. Google Bigtabte with US or EU as location to store the data, and gcloud to access the data.  
D. BigQuery to store the data, and a web server cluster in a managed instance group to access the data. Google Cloud SQL mirrored across two distinct regions to store the data, and a Redis cluster in a managed instance group to access the data.    
  
[Discussion](/assets/gcp/discussion/272.md)  
[Answers and Votes](/assets/gcp/discussion/272.ans.html)  

  
# 273    

Question  
The current Dress4Win system architecture has high latency to some customers because it is located in one data center.  
As of a future evaluation and optimizing for performance in the cloud, Dresss4Win wants to distribute its system architecture to multiple locations when Google cloud platform.  
Which approach should they use?          

A. Use regional managed instance groups and a global load balancer to increase performance because the regional managed instance group can grow instances in each region separately based on traffic.  
B. Use a global load balancer with a set of virtual machines that forward the requests to a closer group of virtual machines managed by your operations team.  
C. Use regional managed instance groups and a global load balancer to increase reliability by providing automatic failover between zones in different regions.  
D. Use a global load balancer with a set of virtual machines that forward the requests to a closer group of virtual machines as part of a separate managed instance groups.    
  
[Discussion](/assets/gcp/discussion/273.md)  
[Answers and Votes](/assets/gcp/discussion/273.ans.html)  

  
# 274    

Question  
For this question, refer to the Dress4Win case study. Dress4Win is expected to grow to 10 times its size in 1 year with a corresponding growth in data and traffic that mirrors the existing patterns of usage. The CIO has set the target of migrating production infrastructure to the cloud within the next 6 months. How will you configure the solution to scale for this growth without making major application changes and still maximize the ROI?          

A. Migrate the web application layer to App Engine, and MySQL to Cloud Datastore, and NAS to Cloud Storage. Deploy RabbitMQ, and deploy Hadoop servers using Deployment Manager.  
B. Migrate RabbitMQ to Cloud Pub/Sub, Hadoop to BigQuery, and NAS to Compute Engine with Persistent Disk storage. Deploy Tomcat, and deploy Nginx using Deployment Manager.  
C. Implement managed instance groups for Tomcat and Nginx. Migrate MySQL to Cloud SQL, RabbitMQ to Cloud Pub/Sub, Hadoop to Cloud Dataproc, and NAS to Compute Engine with Persistent Disk storage.  
D. Implement managed instance groups for the Tomcat and Nginx. Migrate MySQL to Cloud SQL, RabbitMQ to Cloud Pub/Sub, Hadoop to Cloud Dataproc, and NAS to Cloud Storage.    
    
  
[Discussion](/assets/gcp/discussion/274.md)  
[Answers and Votes](/assets/gcp/discussion/274.ans.html)  

  
# 275    

Question
For this question, refer to the Dress4Win case study. Considering the given business requirements, how would you automate the deployment of web and transactional data layers?          

A. Deploy Nginx and Tomcat using Cloud Deployment Manager to Compute Engine. Deploy a Cloud SQL server to replace MySQL. Deploy Jenkins using Cloud Deployment Manager.  
B. Deploy Nginx and Tomcat using Cloud Launcher. Deploy a MySQL server using Cloud Launcher. Deploy Jenkins to Compute Engine using Cloud Deployment Manager scripts.  
C. Migrate Nginx and Tomcat to App Engine. Deploy a Cloud Datastore server to replace the MySQL server in a high-availability configuration. Deploy Jenkins to Compute Engine using Cloud Launcher.
D. Migrate Nginx and Tomcat to App Engine. Deploy a MySQL server using Cloud Launcher. Deploy Jenkins to Compute Engine using Cloud Launcher.    
  
[Discussion](/assets/gcp/discussion/275.md)  
[Answers and Votes](/assets/gcp/discussion/275.ans.html)  

  
# 276    

Question  
For this question, refer to the Dress4Win case study. Which of the compute services should be migrated as-is and would still be an optimized architecture for performance in the cloud?          

A. Web applications deployed using App Engine standard environment  
B. RabbitMQ deployed using an unmanaged instance group  
C. Hadoop/Spark deployed using Cloud Dataproc Regional in High Availability mode  
D. Jenkins, monitoring, bastion hosts, security scanners services deployed on custom machine types    
  
[Discussion](/assets/gcp/discussion/276.md)  
[Answers and Votes](/assets/gcp/discussion/276.ans.html)  

  
# 277    

Question  
For this question, refer to the Dress4Win case study. To be legally compliant during an audit, Dress4Win must be able to give insights in all administrative actions that modify the configuration or metadata of resources on Google Cloud.  
What should you do?          

A. Use Stackdriver Trace to create a Trace list analysis.  
B. Use Stackdriver Monitoring to create a dashboard on the project's activity.  
C. Enable Cloud Identity-Aware Proxy in all projects, and add the group of Administrators as a member.  
D. Use the Activity page in the GCP Console and Stackdriver Logging to provide the required insight.    
  
[Discussion](/assets/gcp/discussion/277.md)  
[Answers and Votes](/assets/gcp/discussion/277.ans.html)  

  
# 278    

Question  
For this question, refer to the Dress4Win case study. You are responsible for the security of data stored in Cloud Storage for your company, Dress4Win. You have already created a set of Google Groups and assigned the appropriate users to those groups. You should use Google best practices and implement the simplest design to meet the requirements.  
Considering Dress4Win's business and technical requirements, what should you do?          

A. Assign custom IAM roles to the Google Groups you created in order to enforce security requirements. Encrypt data with a customer-supplied encryption key when storing files in Cloud Storage.  
B. Assign custom IAM roles to the Google Groups you created in order to enforce security requirements. Enable default storage encryption before storing files in Cloud Storage.  
C. Assign predefined IAM roles to the Google Groups you created in order to enforce security requirements. Utilize Google's default encryption at rest when storing files in Cloud Storage.  
D. Assign predefined IAM roles to the Google Groups you created in order to enforce security requirements. Ensure that the default Cloud KMS key is set before storing files in Cloud Storage.    
  
[Discussion](/assets/gcp/discussion/278.md)  
[Answers and Votes](/assets/gcp/discussion/278.ans.html)  

  
# 279    

Question
For this question, refer to the Dress4Win case study. You want to ensure that your on-premises architecture meets business requirements before you migrate your solution.  
What change in the on-premises architecture should you make?          

A. Replace RabbitMQ with Google Pub/Sub.  
B. Downgrade MySQL to v5.7, which is supported by Cloud SQL for MySQL.  
C. Resize compute resources to match predefined Compute Engine machine types.  
D. Containerize the micro-services and host them in Google Kubernetes Engine.    
  
[Discussion](/assets/gcp/discussion/279.md)  
[Answers and Votes](/assets/gcp/discussion/279.ans.html)  

  
