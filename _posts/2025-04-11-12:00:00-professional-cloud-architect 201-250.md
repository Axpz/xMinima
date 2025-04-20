---
layout: home
title: "professional cloud architect 201-250"
date: 2025-04-11 12:00:00 +0800
lastupdated: 2025-04-11 12:00:00 +0800
categories: cloud
tags: [ai,k8s,cloud]
---
professional cloud architect 2025-04-11 12:00:00
  
# 201

Introductory Info
Company Overview -
JencoMart is a global retailer with over 10,000 stores in 16 countries. The stores carry a range of goods, such as groceries, tires, and jewelry. One of the company's core values is excellent customer service. In addition, they recently introduced an environmental policy to reduce their carbon output by 50% over the next 5 years.  

Company Background -
JencoMart started as a general store in 1931, and has grown into one of the world's leading brands, known for great value and customer service. Over time, the company transitioned from only physical stores to a stores and online hybrid model, with 25% of sales online. Currently, JencoMart has little presence in Asia, but considers that market key for future growth.  

Solution Concept -
JencoMart wants to migrate several critical applications to the cloud but has not completed a technical review to determine their suitability for the cloud and the engineering required for migration. They currently host all of these applications on infrastructure that is at its end of life and is no longer supported.  

Existing Technical Environment -
JencoMart hosts all of its applications in 4 data centers: 3 in North American and 1 in Europe; most applications are dual-homed.
JencoMart understands the dependencies and resource usage metrics of their on-premises architecture.
Application: Customer loyalty portal
LAMP (Linux, Apache, MySQL and PHP) application served from the two JencoMart-owned U.S. data centers.  

Database -
Oracle Database stores user profiles
- 20 TB
- Complex table structure
- Well maintained, clean data
- Strong backup strategy
PostgreSQL database stores user credentials
- Single-homed in US West
- No redundancy
- Backed up every 12 hours
- 100% uptime service level agreement (SLA)  
- Authenticates all users

Compute -
30 machines in US West Coast, each machine has:  
- Twin, dual core CPUs
- 32 GB of RAM
- Twin 250 GB HDD (RAID 1)
20 machines in US East Coast, each machine has:  
- Single, dual-core CPU
- 24 GB of RAM
- Twin 250 GB HDD (RAID 1)  

Storage -
Access to shared 100 TB SAN in each location
Tape backup every week

Business Requirements -
Optimize for capacity during peak periods and value during off-peak periods
Guarantee service availability and support
Reduce on-premises footprint and associated financial and environmental impact
Move to outsourcing model to avoid large upfront costs associated with infrastructure purchase
Expand services into Asia

Technical Requirements -
Assess key application for cloud suitability
Modify applications for the cloud
Move applications to a new infrastructure
Leverage managed services wherever feasible
Sunset 20% of capacity in existing data centers
Decrease latency in Asia

CEO Statement -
JencoMart will continue to develop personal relationships with our customers as more people access the web. The future of our retail business is in the global market and the connection between online and in-store experiences. As a large, global company, we also have a responsibility to the environment through `green` initiatives and policies.  

CTO Statement -
The challenges of operating data centers prevent focus on key technologies critical to our long-term success. Migrating our data services to a public cloud infrastructure will allow us to focus on big data and machine learning to improve our service to customers.  

CFO Statement -
Since its founding, JencoMart has invested heavily in our data services infrastructure. However, because of changing market trends, we need to outsource our infrastructure to ensure our long-term success. This model will allow us to respond to increasing customer demand during peak periods and reduce costs.  
  
Question  
The JencoMart security team requires that all Google Cloud Platform infrastructure is deployed using a least privilege model with separation of duties for administration between production and development resources.  
What Google domain and project structure should you recommend?          

A. Create two G Suite accounts to manage users: one for development/test/staging and one for production. Each account should contain one project for every application  
B. Create two G Suite accounts to manage users: one with a single project for all development applications and one with a single project for all production applications  
C. Create a single G Suite account to manage users with each stage of each application in its own project  
D. Create a single G Suite account to manage users with one project for the development/test/staging environment and one project for the production environment     
  
[Discussion](/assets/gcp/discussion/201.md)  
  
# 202
  
Question  
A few days after JencoMart migrates the user credentials database to Google Cloud Platform and shuts down the old server, the new database server stops responding to SSH connections. It is still serving database requests to the application servers correctly.  
What three steps should you take to diagnose the problem?       (Choose three.)    

A. Delete the virtual machine (VM) and disks and create a new one  
B. Delete the instance, attach the disk to a new VM, and investigate  
C. Take a snapshot of the disk and connect to a new machine to investigate  
D. Check inbound firewall rules for the network the machine is connected to  
E. Connect the machine to another network with very simple firewall rules and investigate  
F. Print the Serial Console output for the instance for troubleshooting, activate the interactive console, and investigate    
  
[Discussion](/assets/gcp/discussion/202.md)  
[Answers and Votes](/assets/gcp/discussion/202.ans.html)  

  
# 203

Question
JencoMart has decided to migrate user profile storage to Google Cloud Datastore and the application servers to Google Compute Engine (GCE). During the migration, the existing infrastructure will need access to Datastore to upload the data.
What service account key-management strategy should you recommend?        

A. Provision service account keys for the on-premises infrastructure and for the GCE virtual machines (VMs)  
B. Authenticate the on-premises infrastructure with a user account and provision service account keys for the VMs  
C. Provision service account keys for the on-premises infrastructure and use Google Cloud Platform (GCP) managed keys for the VMs  
D. Deploy a custom authentication service on GCE/Google Kubernetes Engine (GKE) for the on-premises infrastructure and use GCP managed keys for the VMs   
  
[Discussion](/assets/gcp/discussion/203.md)  
[Answers and Votes](/assets/gcp/discussion/203.ans.html)  
[Service account keys vs Google Cloud Platform (GCP) managed keys](/assets/gcp/discussion/203.vs.html)  
  
# 204

Question  
JencoMart has built a version of their application on Google Cloud Platform that serves traffic to Asia. You want to measure success against their business and technical goals.  
Which metrics should you track?          

A. Error rates for requests from Asia  
B. Latency difference between US and Asia  
C. Total visits, error rates, and latency from Asia  
D. Total visits and average latency for users from Asia  
E. The number of character sets present in the database    
  
[Discussion](/assets/gcp/discussion/204.md)  
[Answers and Votes](/assets/gcp/discussion/204.ans.html)  

  
# 205   
  

The migration of JencoMart's application to Google Cloud Platform (GCP) is progressing too slowly. The infrastructure is shown in the diagram. You want to maximize throughput.
What are three potential bottlenecks?       (Choose three.)  
  
![image](/assets/images/n8n/205.png)  
  
  

A. A single VPN tunnel, which limits throughput  
B. A tier of Google Cloud Storage that is not suited for this task  
C. A copy command that is not suited to operate over long distances  
D. Fewer virtual machines (VMs) in GCP than on-premises machines  
E. A separate storage layer outside the VMs, which is not suited for this task  
F. Complicated internet connectivity between the on-premises infrastructure and GCP    
  
[Discussion](/assets/gcp/discussion/205.md)  
[Answers and Votes](/assets/gcp/discussion/205.ans.html)  

  
# 206
  
Question  
JencoMart wants to move their User Profiles database to Google Cloud Platform.  
Which Google Database should they use?          

A. Cloud Spanner  
B. Google BigQuery  
C. Google Cloud SQL  
D. Google Cloud Datastore    
  
[Discussion](/assets/gcp/discussion/206.md)  
[Discussion](/assets/gcp/discussion/206.ans.html)  
  
# 207

Introductory Info  
Company overview -  
Helicopter Racing League (HRL) is a global sports league for competitive helicopter racing. Each year HRL holds the world championship and several regional league competitions where teams compete to earn a spot in the world championship. HRL offers a paid service to stream the races all over the world with live telemetry and predictions throughout each race.  

Solution concept -  
HRL wants to migrate their existing service to a new platform to expand their use of managed AI and ML services to facilitate race predictions. Additionally, as new fans engage with the sport, particularly in emerging regions, they want to move the serving of their content, both real-time and recorded, closer to their users.  

Existing technical environment -  
HRL is a public cloud-first company; the core of their mission-critical applications runs on their current public cloud provider. Video recording and editing is performed at the race tracks, and the content is encoded and transcoded, where needed, in the cloud. Enterprise-grade connectivity and local compute is provided by truck-mounted mobile data centers. Their race prediction services are hosted exclusively on their existing public cloud provider. Their existing technical environment is as follows:  
Existing content is stored in an object storage service on their existing public cloud provider.  
Video encoding and transcoding is performed on VMs created for each job.  
Race predictions are performed using TensorFlow running on VMs in the current public cloud provider.  

Business requirements -  
HRL's owners want to expand their predictive capabilities and reduce latency for their viewers in emerging markets. Their requirements are:  
Support ability to expose the predictive models to partners.  
Increase predictive capabilities during and before races:  
ג—‹ Race results  
ג—‹ Mechanical failures  
ג—‹ Crowd sentiment  
Increase telemetry and create additional insights.  
Measure fan engagement with new predictions.  
Enhance global availability and quality of the broadcasts.  
Increase the number of concurrent viewers.  
Minimize operational complexity.  
Ensure compliance with regulations.  
Create a merchandising revenue stream.    

Technical requirements -  
Maintain or increase prediction throughput and accuracy.  
Reduce viewer latency.  
Increase transcoding performance.  
Create real-time analytics of viewer consumption patterns and engagement.  
Create a data mart to enable processing of large volumes of race data.    

Executive statement -
Our CEO, S. Hawke, wants to bring high-adrenaline racing to fans all around the world. We listen to our fans, and they want enhanced video streams that include predictions of events within the race (e.g., overtaking). Our current platform allows us to predict race outcomes but lacks the facility to support real-time predictions during races and the capacity to process season-long results.  
  
Question  
For this question, refer to the Helicopter Racing League (HRL) case study. Your team is in charge of creating a payment card data vault for card numbers used to bill tens of thousands of viewers, merchandise consumers, and season ticket holders. You need to implement a custom card tokenization service that meets the following requirements:  
* It must provide low latency at minimal cost.  
* It must be able to identify duplicate credit cards and must not store plaintext card numbers.  
* It should support annual key rotation.  
Which storage approach should you adopt for your tokenization service?         
  
  
A. Store the card data in Secret Manager after running a query to identify duplicates.  
B. Encrypt the card data with a deterministic algorithm stored in Firestore using Datastore mode.  
C. Encrypt the card data with a deterministic algorithm and shard it across multiple Memorystore instances.  
D. Use column-level encryption to store the data in Cloud SQL.  
  
[Discussion](/assets/gcp/discussion/207.md)  
[Answers and Votes](/assets/gcp/discussion/207.ans.html)  
  
# 208

Question
For this question, refer to the Helicopter Racing League (HRL) case study. Recently HRL started a new regional racing league in Cape Town, South Africa. In an effort to give customers in Cape Town a better user experience, HRL has partnered with the Content Delivery Network provider, Fastly. HRL needs to allow traffic coming from all of the Fastly IP address ranges into their Virtual Private Cloud network (VPC network). You are a member of the HRL security team and you need to configure the update that will allow only the Fastly IP address ranges through the External HTTP(S) load balancer. Which command should you use?          

A. gcloud compute security-policies rules update 1000 \  
  --security-policy from-fastly \  
  --src-ip-ranges * \  
  --action "allow"  
B. gcloud compute firewall rules update sourceiplist-fastly \  
  --priority 1000 \  
  --allow tcp:443  
C. gcloud compute firewall rules update hlr-policy \  
  --priority 1000 \  
  --target-tags=sourceiplist-fastly \  
  --allow tcp:443  
D. gcloud compute security-policies rules update 1000 \  
  --security-policy hlr-policy \  
  --expression "evaluatePreconfiguredExpr('sourceiplist-fastly')" \  
  --action "allow"    
  
[Discussion](/assets/gcp/discussion/208.md)  
  
# 209
  
Question
For this question, refer to the Helicopter Racing League (HRL) case study. The HRL development team releases a new version of their predictive capability application every Tuesday evening at 3 a.m. UTC to a repository. The security team at HRL has developed an in-house penetration test Cloud Function called Airwolf. The security team wants to run Airwolf against the predictive capability application as soon as it is released every Tuesday. You need to set up Airwolf to run at the recurring weekly cadence. What should you do?          

A. Set up Cloud Tasks and a Cloud Storage bucket that triggers a Cloud Function.  
B. Set up a Cloud Logging sink and a Cloud Storage bucket that triggers a Cloud Function.  
C. Configure the deployment job to notify a Pub/Sub queue that triggers a Cloud Function.  
D. Set up Identity and Access Management (IAM) and Confidential Computing to trigger a Cloud Function.    
  
[Discussion](/assets/gcp/discussion/209.md)    
[Answers and Votes](/assets/gcp/discussion/209.ans.html)    
  
# 210
  
Question  
For this question, refer to the Helicopter Racing League (HRL) case study. HRL wants better prediction accuracy from their ML prediction models. They want you to use Google's AI Platform so HRL can understand and interpret the predictions. What should you do?          

A. Use Explainable AI.  
B. Use Vision AI.  
C. Use Google Cloud's operations suite.  
D. Use Jupyter Notebooks.    
  
[Discussion](/assets/gcp/discussion/210.md)  
[Answers and Votes](/assets/gcp/discussion/210.ans.html)    

  
# 211

Question  
For this question, refer to the Helicopter Racing League (HRL) case study. HRL is looking for a cost-effective approach for storing their race data such as telemetry. They want to keep all historical records, train models using only the previous season's data, and plan for data growth in terms of volume and information collected. You need to propose a data solution. Considering HRL business requirements and the goals expressed by CEO S. Hawke, what should you do?          

A. Use Firestore for its scalable and flexible document-based database. Use collections to aggregate race data by season and event.  
B. Use Cloud Spanner for its scalability and ability to version schemas with zero downtime. Split race data using season as a primary key.  
C. Use BigQuery for its scalability and ability to add columns to a schema. Partition race data based on season.  
D. Use Cloud SQL for its ability to automatically manage storage increases and compatibility with MySQL. Use separate database instances for each season.    
  
[Discussion](/assets/gcp/discussion/211.md)  
[Answers and Votes](/assets/gcp/discussion/211.ans.html)  
  
# 212

Question
For this question, refer to the Helicopter Racing League (HRL) case study. A recent finance audit of cloud infrastructure noted an exceptionally high number of Compute Engine instances are allocated to do video encoding and transcoding. You suspect that these Virtual Machines are zombie machines that were not deleted after their workloads completed. You need to quickly get a list of which VM instances are idle. What should you do?          

A. Log into each Compute Engine instance and collect disk, CPU, memory, and network usage statistics for analysis.  
B. Use the gcloud compute instances list to list the virtual machine instances that have the idle: true label set.  
C. Use the gcloud recommender command to list the idle virtual machine instances.  
D. From the Google Console, identify which Compute Engine instances in the managed instance groups are no longer responding to health check probes.    
  
[Discussion](/assets/gcp/discussion/212.md)  
  
# 213

Question  
For this question, refer to the EHR Healthcare case study. You are responsible for ensuring that EHR's use of Google Cloud will pass an upcoming privacy compliance audit. What should you do?       (Choose two.)    

A. Verify EHR's product usage against the list of compliant products on the Google Cloud compliance page.  
B. Advise EHR to execute a Business Associate Agreement (BAA) with Google Cloud.  
C. Use Firebase Authentication for EHR's user facing applications.  
D. Implement Prometheus to detect and prevent security breaches on EHR's web-based applications.  
E. Use GKE private clusters for all Kubernetes workloads.  
  
[Discussion](/assets/gcp/discussion/213.md)  
[Answers and Votes](/assets/gcp/discussion/213.ans.html)  

  
# 214

Question
For this question, refer to the EHR Healthcare case study. You need to define the technical architecture for securely deploying workloads to Google Cloud. You also need to ensure that only verified containers are deployed using Google Cloud services. What should you do?       (Choose two.)    

A. Enable Binary Authorization on GKE, and sign containers as part of a CI/CD pipeline.  
B. Configure Jenkins to utilize Kritis to cryptographically sign a container as part of a CI/CD pipeline.  
C. Configure Container Registry to only allow trusted service accounts to create and deploy containers from the registry.  
D. Configure Container Registry to use vulnerability scanning to confirm that there are no vulnerabilities before deploying the workload.    
  
[Discussion](/assets/gcp/discussion/214.md)  
[Answers and Votes](/assets/gcp/discussion/214.ans.html)  

  
# 215

Question
You need to upgrade the EHR connection to comply with their requirements. The new connection design must support business-critical needs and meet the same network and security policy requirements. What should you do?          

A. Add a new Dedicated Interconnect connection.  
B. Upgrade the bandwidth on the Dedicated Interconnect connection to 100 G.  
C. Add three new Cloud VPN connections.  
D. Add a new Carrier Peering connection.    
  
[Discussion](/assets/gcp/discussion/215.md)  
[Answers and Votes](/assets/gcp/discussion/215.ans.html)  
[99.99% HA](https://cloud.google.com/network-connectivity/docs/interconnect/images/9999-availability.svg
)  



  
# 216

Question
For this question, refer to the EHR Healthcare case study. You need to define the technical architecture for hybrid connectivity between EHR's on-premises systems and Google Cloud. You want to follow Google's recommended practices for production-level applications. Considering the EHR Healthcare business and technical requirements, what should you do?          

A. Configure two Partner Interconnect connections in one metro (City), and make sure the Interconnect connections are placed in different metro zones.  
B. Configure two VPN connections from on-premises to Google Cloud, and make sure the VPN devices on-premises are in separate racks.  
C. Configure Direct Peering between EHR Healthcare and Google Cloud, and make sure you are peering at least two Google locations.  
D. Configure two Dedicated Interconnect connections in one metro (City) and two connections in another metro, and make sure the Interconnect connections are placed in different metro zones.    
  
[Discussion](/assets/gcp/discussion/216.md)  
[Answers and Votes](/assets/gcp/discussion/216.ans.html)  

  
# 217

Question
For this question, refer to the EHR Healthcare case study. You are a developer on the EHR customer portal team. Your team recently migrated the customer portal application to Google Cloud. The load has increased on the application servers, and now the application is logging many timeout errors. You recently incorporated Pub/Sub into the application architecture, and the application is not logging any Pub/Sub publishing errors. You want to improve publishing latency.  
What should you do?          

A. Increase the Pub/Sub Total Timeout retry value.  
B. Move from a Pub/Sub subscriber pull model to a push model.    
C. Turn off Pub/Sub message batching.  
D. Create a backup Pub/Sub message queue.    
  
[Discussion](/assets/gcp/discussion/217.md)  
[Answers and Votes](/assets/gcp/discussion/217.ans.html)  

  
# 218

Question  
For this question, refer to the EHR Healthcare case study. In the past, configuration errors put public IP addresses on backend servers that should not have been accessible from the Internet. You need to ensure that no one can put external IP addresses on backend Compute Engine instances and that external IP addresses can only be configured on frontend Compute Engine instances. What should you do?          

A. Create an Organizational Policy with a constraint to allow external IP addresses only on the frontend Compute Engine instances.  
B. Revoke the compute.networkAdmin role from all users in the project with front end instances.  
C. Create an Identity and Access Management (IAM) policy that maps the IT staff to the compute.networkAdmin role for the organization.  
D. Create a custom Identity and Access Management (IAM) role named GCE_FRONTEND with the compute.addresses.create permission.    
  
[Discussion](/assets/gcp/discussion/218.md)  
[Answers and Votes](/assets/gcp/discussion/218.ans.html)  

  
# 219

Question  
For this question, refer to the EHR Healthcare case study.   
You are responsible for designing the Google Cloud network architecture for Google Kubernetes  
Engine. You want to follow Google best practices. Considering the EHR Healthcare business and technical requirements, what should you do to reduce the attack surface?          

A. Use a private cluster with a private endpoint with master authorized networks configured.  
B. Use a public cluster with firewall rules and Virtual Private Cloud (VPC) routes.  
C. Use a private cluster with a public endpoint with master authorized networks configured.  
D. Use a public cluster with master authorized networks enabled and firewall rules.    
  
  
[Discussion](/assets/gcp/discussion/219.md)  
  
# 220

Introductory Info  
Company Overview -  
Mountkirk Games makes online, session-based, multiplayer games for the most popular mobile platforms. They build all of their games using some server-side integration. Historically, they have used cloud providers to lease physical servers.  
Due to the unexpected popularity of some of their games, they have had problems scaling their global audience, application servers MySQL databases, and analytics tools.  
Their current model is to write game statistics to files and send them through an ETL tool that loads them into a centralized MySQL database for reporting.    

Solution Concept -  
Mountkirk Games is building a new game, which they expect to be very popular. They plan to deploy the game's backend on Google Compute Engine so they can capture streaming metrics run intensive analytics, and take advantage of its autoscaling server environment and integrate with a managed NoSQL database.    

Business Requirements -  
Increase to a global footprint  
Improve uptime " downtime is loss of players  
Increase efficiency of the cloud resources we use  
Reduce latency to all customers    

Technical Requirements -  
Requirements for Game Backend Platform  
1. Dynamically scale up or down based on game activity  
2. Connect to a managed NoSQL database service  
3. Run customize Linux distro  

Requirements for Game Analytics Platform  
1. Dynamically scale up or down based on game activity  
2. Process incoming data on the fly directly from the game servers  
3. Process data that arrives late because of slow mobile networks  
4. Allow SQL queries to access at least 10 TB of historical data  
5. Process files that are regularly uploaded by users' mobile devices  
6. Use only fully managed services    

CEO Statement -  
Our last successful game did not scale well with our previous cloud provider, resulting in lower user adoption and affecting the game's reputation. Our investors want more key performance indicators (KPIs) to evaluate the speed and stability of the game, as well as other metrics that provide deeper insight into usage patterns so we can adapt the game to target users.    

CTO Statement -  
Our current technology stack cannot provide the scale we need, so we want to replace MySQL and move to an environment that provides autoscaling, low latency load balancing, and frees us up from managing physical servers.    

CFO Statement -  
We are not capturing enough user demographic data, usage metrics, and other KPIs. As a result, we do not engage the right users, we are not confident that our marketing is targeting the right users, and we are not selling enough premium Blast-Ups inside the games, which dramatically impacts our revenue.  
Question  
Mountkirk Games wants you to design their new testing strategy. How should the test coverage differ from their existing backends on the other platforms?          

A. Tests should scale well beyond the prior approaches  
B. Unit tests are no longer required, only end-to-end tests  
C. Tests should be applied after the release is in the production environment  
D. Tests should include directly testing the Google Cloud Platform (GCP) infrastructure    
  
  
[Discussion](/assets/gcp/discussion/220.md)  
[Answers and Votes](/assets/gcp/discussion/220.ans.html)  
  
# 221

Question  
Mountkirk Games has deployed their new backend on Google Cloud Platform (GCP).   
You want to create a through testing process for new versions of the backend before they are released to the public. You want the testing environment to scale in an economical way. How should you design the process?          

A. Create a scalable environment in GCP for simulating production load  
B. Use the existing infrastructure to test the GCP-based backend at scale  
C. Build stress tests into each component of your application using resources internal to GCP to simulate load  
D. Create a set of static environments in GCP to test different levels of load ג€" for example, high, medium, and low    
  
[Discussion](/assets/gcp/discussion/221.md)  
[Answers and Votes](/assets/gcp/discussion/221.ans.html)  

  
# 222

Question  
Mountkirk Games wants to set up a continuous delivery pipeline. Their architecture includes many small services that they want to be able to update and roll back quickly. Mountkirk Games has the following requirements:  
✑ Services are deployed redundantly across multiple regions in the US and Europe  
✑ Only frontend services are exposed on the public internet  
✑ They can provide a single frontend IP for their fleet of services  
✑ Deployment artifacts are immutable  
Which set of products should they use?          

A. Google Cloud Storage, Google Cloud Dataflow, Google Compute Engine  
B. Google Cloud Storage, Google App Engine, Google Network Load Balancer  
C. Google Kubernetes Registry, Google Container Engine, Google HTTP(S) Load Balancer  
D. Google Cloud Functions, Google Cloud Pub/Sub, Google Cloud Deployment Manager  
   
[Discussion](/assets/gcp/discussion/222.md)   
[Answers and Votes](/assets/gcp/discussion/222.ans.html)   

  
# 223

Question  
Mountkirk Games' gaming servers are not automatically scaling properly.   
Last month, they rolled out a new feature, which suddenly became very popular. A record number of users are trying to use the service, but many of them are getting 503 errors and very slow response times. What should they investigate first?          

A. Verify that the database is online  
B. Verify that the project quota hasn't been exceeded  
C. Verify that the new feature code did not introduce any performance bugs  
D. Verify that the load-testing team is not running their tool against production    
  
[Discussion](/assets/gcp/discussion/223.md)  
[Answers and Votes](/assets/gcp/discussion/223.ans.html)  

  
# 224

Question  
Mountkirk Games needs to create a repeatable and configurable mechanism for deploying isolated application environments. Developers and testers can access each other's environments and resources, but they cannot access staging or production resources. The staging environment needs access to some services from production.  
What should you do to isolate development environments from staging and production?          

A. Create a project for development and test and another for staging and production  
B. Create a network for development and test and another for staging and production  
C. Create one subnetwork for development and another for staging and production  
D. Create one project for development, a second for staging and a third for production    
  
[Discussion](/assets/gcp/discussion/224.md)  
[Answers and Votes](/assets/gcp/discussion/224.ans.html)  

  
# 225

Question  
Mountkirk Games wants to set up a real-time analytics platform for their new game. The new platform must meet their technical requirements.  
Which combination of Google technologies will meet all of their requirements?          

A. Kubernetes Engine, Cloud Pub/Sub, and Cloud SQL  
B. Cloud Dataflow, Cloud Storage, Cloud Pub/Sub, and BigQuery  
C. Cloud SQL, Cloud Storage, Cloud Pub/Sub, and Cloud Dataflow  
D. Cloud Dataproc, Cloud Pub/Sub, Cloud SQL, and Cloud Dataflow  
E. Cloud Pub/Sub, Compute Engine, Cloud Storage, and Cloud Dataproc    
  
[Discussion](/assets/gcp/discussion/225.md)  
[Answers and Votes](/assets/gcp/discussion/225.ans.html)  

  
# 226

Question  
For this question, refer to the Mountkirk Games case study. Mountkirk Games wants to migrate from their current analytics and statistics reporting model to one that meets their technical requirements on Google Cloud Platform.  
Which two steps should be part of their migration plan?       (Choose two.)    

A. Evaluate the impact of migrating their current batch ETL code to Cloud Dataflow.  
B. Write a schema migration plan to denormalize data for better performance in BigQuery.  
C. Draw an architecture diagram that shows how to move from a single MySQL database to a MySQL cluster.  
D. Load 10 TB of analytics data from a previous game into a Cloud SQL instance, and run test queries against the full dataset to confirm that they complete successfully.  
E. Integrate Cloud Armor to defend against possible SQL injection attacks in analytics files uploaded to Cloud Storage.    
  
[Discussion](/assets/gcp/discussion/226.md)  
[Answers and Votes](/assets/gcp/discussion/226.ans.html)  

  
# 227

Question  
For this question, refer to the Mountkirk Games case study. You need to analyze and define the technical architecture for the compute workloads for your company, Mountkirk Games. Considering the Mountkirk Games business and technical requirements, what should you do?          

A. Create network load balancers. Use preemptible Compute Engine instances.  
B. Create network load balancers. Use non-preemptible Compute Engine instances.  
C. Create a global load balancer with managed instance groups and autoscaling policies. Use preemptible Compute Engine instances.  
D. Create a global load balancer with managed instance groups and autoscaling policies. Use non-preemptible Compute Engine instances.    
  
[Discussion](/assets/gcp/discussion/227.md)  
[Answers and Votes](/assets/gcp/discussion/227.ans.html)  
[Global HTTP(S) LB vs Global Load Balancer（总称）vs Network Load Balancer](/assets/gcp/discussion/227.vs.html)  
  
# 228

Question  
For this question, refer to the Mountkirk Games case study. Mountkirk Games wants to design their solution for the future in order to take advantage of cloud and technology improvements as they become available. Which two steps should they take?       (Choose two.)    

A. Store as much analytics and game activity data as financially feasible today so it can be used to train machine learning models to predict user behavior in the future.  
B. Begin packaging their game backend artifacts in container images and running them on Google Kubernetes Engine to improve the ability to scale up or down based on game activity.  
C. Set up a CI/CD pipeline using Jenkins and Spinnaker to automate canary deployments and improve development velocity.  
D. Adopt a schema versioning tool to reduce downtime when adding new game features that require storing additional player data in the database.
E. Implement a weekly rolling maintenance process for the Linux virtual machines so they can apply critical kernel patches and package updates and reduce the risk of 0-day vulnerabilities.    
  
[Discussion](/assets/gcp/discussion/228.md)  
[Answers and Votes](/assets/gcp/discussion/228.ans.html)  

  
# 229

Question  
For this question, refer to the Mountkirk Games case study. Mountkirk Games wants you to design a way to test the analytics platform's resilience to changes in mobile network latency. What should you do?          

A. Deploy failure injection software to the game analytics platform that can inject additional latency to mobile client analytics traffic.  
B. Build a test client that can be run from a mobile phone emulator on a Compute Engine virtual machine, and run multiple copies in Google Cloud Platform regions all over the world to generate realistic traffic.  
C. Add the ability to introduce a random amount of delay before beginning to process analytics files uploaded from mobile devices.  
D. Create an opt-in beta of the game that runs on players' mobile devices and collects response times from analytics endpoints running in Google Cloud Platform regions all over the world.    
  
[Discussion](/assets/gcp/discussion/229.md)  
[Answers and Votes](/assets/gcp/discussion/229.ans.html)  

  
# 230

Question  
For this question, refer to the Mountkirk Games case study. You need to analyze and define the technical architecture for the database workloads for your company, Mountkirk Games. Considering the business and technical requirements, what should you do?          

A. Use Cloud SQL for time series data, and use Cloud Bigtable for historical data queries.  
B. Use Cloud SQL to replace MySQL, and use Cloud Spanner for historical data queries.  
C. Use Cloud Bigtable to replace MySQL, and use BigQuery for historical data queries.  
D. Use Cloud Bigtable for time series data, use Cloud Spanner for transactional data, and use BigQuery for historical data queries.    
  
[Discussion](/assets/gcp/discussion/230.md)  
[Answers and Votes](/assets/gcp/discussion/230.ans.html)  
[对比分析](/assets/gcp/discussion/230.vs.html)  

  
# 231

Question  
For this question, refer to the Mountkirk Games case study. Which managed storage option meets Mountkirk's technical requirement for storing game activity in a time series database service?          

A. Cloud Bigtable  
B. Cloud Spanner  
C. BigQuery  
D. Cloud Datastore    
  
[Discussion](/assets/gcp/discussion/231.md)  
  
# 232

Question    
For this question, refer to the Mountkirk Games case study. You are in charge of the new Game Backend Platform architecture. The game communicates with the backend over a REST API.    
You want to follow Google-recommended practices. How should you design the backend?            

A. Create an instance template for the backend. For every region, deploy it on a multi-zone managed instance group. Use an L4 load balancer.    
B. Create an instance template for the backend. For every region, deploy it on a single-zone managed instance group. Use an L4 load balancer.  
C. Create an instance template for the backend. For every region, deploy it on a multi-zone managed instance group. Use an L7 load balancer.  
D. Create an instance template for the backend. For every region, deploy it on a single-zone managed instance group. Use an L7 load balancer.    
  
[Discussion](/assets/gcp/discussion/232.md)  
  
# 233

Question  
You need to optimize batch file transfers into Cloud Storage for Mountkirk Games' new Google Cloud solution. The batch files contain game statistics that need to be staged in Cloud Storage and be processed by an extract transform load (ETL) tool. What should you do?          

A. Use gsutil to batch move files in sequence.  
B. Use gsutil to batch copy the files in parallel.  
C. Use gsutil to extract the files as the first part of ETL.  
D. Use gsutil to load the files as the last part of ETL.    
  
[Discussion](/assets/gcp/discussion/233.md)  
[Answers and Votes](/assets/gcp/discussion/233.ans.html)  

  
# 234

Question  
You are implementing Firestore for Mountkirk Games. Mountkirk Games wants to give a new game programmatic access to a legacy game's Firestore database.  
Access should be as restricted as possible. What should you do?          

A. Create a service account (SA) in the legacy game's Google Cloud project, add a second SA in the new game's IAM page, and then give the Organization Admin role to both SAs.  
B. Create a service account (SA) in the legacy game's Google Cloud project, give the SA the Organization Admin role, and then give it the Firebase Admin role in both projects.  
C. Create a service account (SA) in the legacy game's Google Cloud project, add this SA in the new game's IAM page, and then give it the Firebase Admin role in both projects.  
D. Create a service account (SA) in the legacy game's Google Cloud project, give it the Firebase Admin role, and then migrate the new game to the legacy game's project.    
  
[Discussion](/assets/gcp/discussion/234.md)  
[Answers and Votes](/assets/gcp/discussion/234.ans.html)  
[Analysis](/assets/gcp/discussion/234.vs.html)  

  
# 235

Question  
Mountkirk Games wants to limit the physical location of resources to their operating Google Cloud regions. What should you do?          

A. Configure an organizational policy which constrains where resources can be deployed.  
B. Configure IAM conditions to limit what resources can be configured.  
C. Configure the quotas for resources in the regions not being used to 0.  
D. Configure a custom alert in Cloud Monitoring so you can disable resources as they are created in other regions.    
  
[Discussion](/assets/gcp/discussion/235.md)  
[Answers and Votes](/assets/gcp/discussion/235.ans.html)  

  
# 236

Question  
You need to implement a network ingress for a new game that meets the defined business and technical requirements. Mountkirk Games wants each regional game instance to be located in multiple Google Cloud regions. What should you do?          

A. Configure a global load balancer connected to a managed instance group running Compute Engine instances.   
B. Configure kubemci with a global load balancer and Google Kubernetes Engine.  
C. Configure a global load balancer with Google Kubernetes Engine.  
D. Configure Ingress for Anthos with a global load balancer and Google Kubernetes Engine.    
  
[Discussion](/assets/gcp/discussion/236.md)  
[Answers and Votes](/assets/gcp/discussion/236.ans.html)  
[ 对比分析 ](/assets/gcp/discussion/236.vs.html)  

  
# 237

Question
Your development teams release new versions of games running on Google Kubernetes Engine (GKE) daily. You want to create service level indicators (SLIs) to evaluate the quality of the new versions from the user's perspective. What should you do?          

A. Create CPU Utilization and Request Latency as service level indicators.  
B. Create GKE CPU Utilization and Memory Utilization as service level indicators.  
C. Create Request Latency and Error Rate as service level indicators.  
D. Create Server Uptime and Error Rate as service level indicators.    
  
[Discussion](/assets/gcp/discussion/237.md)  
[ 对比分析 ](/assets/gcp/discussion/237.vs.html)  

  
# 238
  

Question  
Mountkirk Games wants you to secure the connectivity from the new gaming application platform to Google Cloud. You want to streamline the process and follow
Google-recommended practices. What should you do?          

A. Configure Workload Identity and service accounts to be used by the application platform.  
B. Use Kubernetes Secrets, which are obfuscated by default. Configure these Secrets to be used by the application platform.  
C. Configure Kubernetes Secrets to store the secret, enable Application-Layer Secrets Encryption, and use Cloud Key Management Service (Cloud KMS) to manage the encryption keys. Configure these Secrets to be used by the application platform.  
D. Configure HashiCorp Vault on Compute Engine, and use customer managed encryption keys and Cloud Key Management Service (Cloud KMS) to manage the encryption keys. Configure these Secrets to be used by the application platform.    
  
[Discussion](/assets/gcp/discussion/238.md)  
[Answers and Votes](/assets/gcp/discussion/238.ans.html)  

  
# 239

Question  
Your development team has created a mobile game app. You want to test the new mobile app on Android and iOS devices with a variety of configurations. You need to ensure that testing is efficient and cost-effective. What should you do?          

A. Upload your mobile app to the Firebase Test Lab, and test the mobile app on Android and iOS devices.  
B. Create Android and iOS VMs on Google Cloud, install the mobile app on the VMs, and test the mobile app.  
C. Create Android and iOS containers on Google Kubernetes Engine (GKE), install the mobile app on the containers, and test the mobile app.  
D. Upload your mobile app with different configurations to Firebase Hosting and test each configuration.    
  
[Discussion](/assets/gcp/discussion/239.md)  
  
# 240

Introductory Info  
Company Overview -  
TerramEarth manufactures heavy equipment for the mining and agricultural industries: about 80% of their business is from mining and 20% from agriculture. They currently have over 500 dealers and service centers in 100 countries. Their mission is to build products that make their customers more productive.    

Company background -  
TerramEarth was formed in 1946, when several small, family owned companies combined to retool after World War II. The company cares about their employees and customers and considers them to be extended members of their family.  
TerramEarth is proud of their ability to innovate on their core products and find new markets as their customers' needs change. For the past 20 years, trends in the industry have been largely toward increasing productivity by using larger vehicles with a human operator.    

Solution Concept -  
There are 20 million TerramEarth vehicles in operation that collect 120 fields of data per second. Data is stored locally on the vehicle and can be accessed for analysis when a vehicle is serviced. The data is downloaded via a maintenance port. This same port can be used to adjust operational parameters, allowing the vehicles to be upgraded in the field with new computing modules.  
Approximately 200,000 vehicles are connected to a cellular network, allowing TerramEarth to collect data directly. At a rate of 120 fields of data per second with 22 hours of operation per day, Terram Earth collects a total of about 9 TB/day from these connected vehicles.    

Existing Technical Environment -    
Data Sources:     ---------------- FTP Servers ---> ETL ---> Data Warehouse    
- 推土机 (Bulldozer)    
- 挖掘机 (Excavator)    
- 货运车 (Cargo Truck)    

TerramEarth's existing architecture is composed of Linux-based systems that reside in a data center. These systems gzip CSV files from the field and upload via  
FTP, transform and aggregate them, and place the data in their data warehouse. Because this process takes time, aggregated reports are based on data that is 3 weeks old.  
With this data, TerramEarth has been able to preemptively stock replacement parts and reduce unplanned downtime of their vehicles by 60%. However, because the data is stale, some customers are without their vehicles for up to 4 weeks while they wait for replacement parts.    

Business Requirements -  
Decrease unplanned vehicle downtime to less than 1 week, without increasing the cost of carrying surplus inventory  
Support the dealer network with more data on how their customers use their equipment to better position new products and services  
Have the ability to partner with different companies `" especially with seed and fertilizer suppliers in the fast-growing agricultural business `" to create compelling joint offerings for their customers.    

CEO Statement -  
We have been successful in capitalizing on the trend toward larger vehicles to increase the productivity of our customers. Technological change is occurring rapidly, and TerramEarth has taken advantage of connected devices technology to provide our customers with better services, such as our intelligent farming equipment. With this technology, we have been able to increase farmers' yields by 25%, by using past trends to adjust how our vehicles operate. These advances have led to the rapid growth of our agricultural product line, which we expect will generate 50% of our revenues by 2020.    

CTO Statement -  
Our competitive advantage has always been in the manufacturing process, with our ability to build better vehicles for lower cost than our competitors. However, new products with different approaches are constantly being developed, and I'm concerned that we lack the skills to undergo the next wave of transformations in our industry. Unfortunately, our CEO doesn't take technology obsolescence seriously and he considers the many new companies in our industry to be niche players. My goals are to build our skills while addressing immediate market needs through incremental innovations.  
Question  
TerramEarth's CTO wants to use the raw data from connected vehicles to help identify approximately when a vehicle in the field will have a catastrophic failure.  
You want to allow analysts to centrally query the vehicle data.  
Which architecture should you recommend?          

Correct Answer: A  
The push endpoint can be a load balancer.  
A container cluster can be used.  
Cloud Pub/Sub for Stream Analytics    
![gcp](/assets/gcp/240.png)  
  
  
[Discussion](/assets/gcp/discussion/240.md)  
  
# 241

Question  
The TerramEarth development team wants to create an API to meet the company's business requirements. You want the development team to focus their development effort on business value versus creating a custom framework.
Which method should they use?        

A. Use Google App Engine with Google Cloud Endpoints. Focus on an API for dealers and partners  
B. Use Google App Engine with a JAX-RS Jersey Java-based framework. Focus on an API for the public  
C. Use Google App Engine with the Swagger (Open API Specification) framework. Focus on an API for the public  
D. Use Google Container Engine with a Django Python container. Focus on an API for the public  
E. Use Google Container Engine with a Tomcat container with the Swagger (Open API Specification) framework. Focus on an API for dealers and partners  
  
  
[Discussion](/assets/gcp/discussion/241.md)  
[Answers and Votes](/assets/gcp/discussion/241.ans.html)  
[Google Cloud Endpoints](/assets/gcp/discussion/241.vs.html)  
  
# 242

Question  
Your development team has created a structured API to retrieve vehicle data. They want to allow third parties to develop tools for dealerships that use this vehicle event data. You want to support delegated authorization against this data.  
What should you do?          

A. Build or leverage an OAuth-compatible access control system  
B. Build SAML 2.0 SSO compatibility into your authentication system  
C. Restrict data access based on the source IP address of the partner systems  
D. Create secondary credentials for each dealer that can be given to the trusted third party    
  
[Discussion](/assets/gcp/discussion/242.md)  
[Answers and Votes](/assets/gcp/discussion/242.ans.html)  
[OAuth 2.0 vs SAML 2.0 SSO](/assets/gcp/discussion/242.vs.html)  


  
# 243

Question
TerramEarth plans to connect all 20 million vehicles in the field to the cloud. This increases the volume to 20 million 600 byte records a second for 40 TB an hour.  
How should you design the data ingestion?          

A. Vehicles write data directly to GCS  
B. Vehicles write data directly to Google Cloud Pub/Sub  
C. Vehicles stream data directly to Google BigQuery  
D. Vehicles continue to write data using the existing system (FTP)    
  
[Discussion](/assets/gcp/discussion/243.md)  
[Answers and Votes](/assets/gcp/discussion/243.ans.html)  

  
# 244

Question
You analyzed TerramEarth's business requirement to reduce downtime, and found that they can achieve a majority of time saving by reducing customer's wait time for parts. You decided to focus on reduction of the 3 weeks aggregate reporting time.  
Which modifications to the company's processes should you recommend?          

A. Migrate from CSV to binary format, migrate from FTP to SFTP transport, and develop machine learning analysis of metrics  
B. Migrate from FTP to streaming transport, migrate from CSV to binary format, and develop machine learning analysis of metrics  
C. Increase fleet cellular connectivity to 80%, migrate from FTP to streaming transport, and develop machine learning analysis of metrics  
D. Migrate from FTP to SFTP transport, develop machine learning analysis of metrics, and increase dealer local inventory by a fixed factor    
  
[Discussion](/assets/gcp/discussion/244.md)  
[Answers and Votes](/assets/gcp/discussion/244.ans.html)  

  
# 245

Question  
Which of TerramEarth's legacy enterprise processes will experience significant change as a result of increased Google Cloud Platform adoption?          

A. Opex/capex allocation, LAN changes, capacity planning  
B. Capacity planning, TCO calculations, opex/capex allocation  
C. Capacity planning, utilization measurement, data center expansion  
D. Data Center expansion, TCO calculations, utilization measurement    
  
[Discussion](/assets/gcp/discussion/245.md)  
[Answers and Votes](/assets/gcp/discussion/245.ans.html)  

  
# 246

Question  
To speed up data retrieval, more vehicles will be upgraded to cellular connections and be able to transmit data to the ETL process. The current FTP process is error-prone and restarts the data transfer from the start of the file when connections fail, which happens often. You want to improve the reliability of the solution and minimize data transfer time on the cellular connections.  
What should you do?          

A. Use one Google Container Engine cluster of FTP servers. Save the data to a Multi-Regional bucket. Run the ETL process using data in the bucket  
B. Use multiple Google Container Engine clusters running FTP servers located in different regions. Save the data to Multi-Regional buckets in US, EU, and Asia. Run the ETL process using the data in the bucket  
C. Directly transfer the files to different Google Cloud Multi-Regional Storage bucket locations in US, EU, and Asia using Google APIs over HTTP(S). Run the ETL process using the data in the bucket  
D. Directly transfer the files to a different Google Cloud Regional Storage bucket location in US, EU, and Asia using Google APIs over HTTP(S). Run the ETL process to retrieve the data from each Regional bucket    
  
[Discussion](/assets/gcp/discussion/246.md)  
[Answers and Votes](/assets/gcp/discussion/246.ans.html)  

  
# 247

Question  
TerramEarth's 20 million vehicles are scattered around the world. Based on the vehicle's location, its telemetry data is stored in a Google Cloud Storage (GCS) regional bucket (US, Europe, or Asia). The CTO has asked you to run a report on the raw telemetry data to determine why vehicles are breaking down after 100 K miles. You want to run this job on all the data.  
What is the most cost-effective way to run this job?          

A. Move all the data into 1 zone, then launch a Cloud Dataproc cluster to run the job  
B. Move all the data into 1 region, then launch a Google Cloud Dataproc cluster to run the job  
C. Launch a cluster in each region to preprocess and compress the raw data, then move the data into a multi-region bucket and use a Dataproc cluster to finish the job  
D. Launch a cluster in each region to preprocess and compress the raw data, then move the data into a region bucket and use a Cloud Dataproc cluster to finish the job    
   
  
  
[Discussion](/assets/gcp/discussion/247.md)  
[Answers and Votes](/assets/gcp/discussion/247.ans.html)  

  
# 248

Question
TerramEarth has equipped all connected trucks with servers and sensors to collect telemetry data. Next year they want to use the data to train machine learning models. They want to store this data in the cloud while reducing costs.  
What should they do?          

A. Have the vehicle's computer compress the data in hourly snapshots, and store it in a Google Cloud Storage (GCS) Nearline bucket  
B. Push the telemetry data in real-time to a streaming dataflow job that compresses the data, and store it in Google BigQuery  
C. Push the telemetry data in real-time to a streaming dataflow job that compresses the data, and store it in Cloud Bigtable  
D. Have the vehicle's computer compress the data in hourly snapshots, and store it in a GCS Coldline bucket    
  
[Discussion](/assets/gcp/discussion/248.md)  
[Answers and Votes](/assets/gcp/discussion/248.ans.html)  

  
# 249

Question
Your agricultural division is experimenting with fully autonomous vehicles. You want your architecture to promote strong security during vehicle operation.  
Which two architectures should you consider?       (Choose two.)    

A. Treat every micro service call between modules on the vehicle as untrusted.  
B. Require IPv6 for connectivity to ensure a secure address space.  
C. Use a trusted platform module (TPM) and verify firmware and binaries on boot.  
D. Use a functional programming language to isolate code execution cycles.  
E. Use multiple connectivity subsystems for redundancy.  
F. Enclose the vehicle's drive electronics in a Faraday cage to isolate chips.    
  
[Discussion](/assets/gcp/discussion/249.md)  
[Answers and Votes](/assets/gcp/discussion/249.ans.html)  

  
# 250

Question  
Operational parameters such as oil pressure are adjustable on each of TerramEarth's vehicles to increase their efficiency, depending on their environmental conditions. Your primary goal is to increase the operating efficiency of all 20 million cellular and unconnected vehicles in the field.  
How can you accomplish this goal?          

A. Have you engineers inspect the data for patterns, and then create an algorithm with rules that make operational adjustments automatically  
B. Capture all operating data, train machine learning models that identify ideal operations, and run locally to make operational adjustments automatically  
C. Implement a Google Cloud Dataflow streaming job with a sliding window, and use Google Cloud Messaging (GCM) to make operational adjustments automatically  
D. Capture all operating data, train machine learning models that identify ideal operations, and host in Google Cloud Machine Learning (ML) Platform to make operational adjustments automatically    
  
[Discussion](/assets/gcp/discussion/250.md)  
[Answers and Votes](/assets/gcp/discussion/250.ans.html)  

