---
layout: home
title: "professional cloud architect 1-50"
date: 2025-04-08 12:00:00 +0800
lastupdated: 2025-04-08 12:00:00 +0800
categories: cloud
tags: [ai,k8s,cloud]
---
professional cloud architect 2025-04-08 12:00:00

# 1

Your company has decided to make a major revision of their API in order to create better experiences for their developers. They need to keep the old version of the API available and deployable, while allowing new customers and testers to try out the new API. They want to keep the same SSL and DNS records in place to serve both APIs.   
What should they do?            

A. Configure a new load balancer for the new version of the API  
B. Reconfigure old clients to use a new endpoint for the new API   
C. Have the old API forward traffic to the new API based on the path  
D. Use separate backend pools for each API path behind the load balancer    

[Discussion](/assets/gcp/discussion/1.md)   
[Answer and Vote](/assets/gcp/discussion/1.ans.html)   


# 2

Your company plans to migrate a multi-petabyte data set to the cloud. The data set must be available 24hrs a day. Your business analysts have experience only with using a SQL interface.
How should you store the data to optimize it for ease of analysis?          

A. Load data into Google BigQuery  
B. Insert data into Google Cloud SQL  
C. Put flat files into Google Cloud Storage  
D. Stream data into Google Cloud Datastore    

[Discussion](/assets/gcp/discussion/2.md)   
[Answer and Vote](/assets/gcp/discussion/2.ans.html)   


# 3

The operations manager asks you for a list of recommended practices that she should consider when migrating a J2EE application to the cloud.  
Which three practices should you recommend?       (Choose three.)    

A. Port the application code to run on Google App Engine  
B. Integrate Cloud Dataflow into the application to capture real-time metrics  
C. Instrument the application with a monitoring tool like Stackdriver Debugger  
D. Select an automation framework to reliably provision the cloud infrastructure  
E. Deploy a continuous integration tool with automated testing in a staging environment  
F. Migrate from MySQL to a managed NoSQL database like Google Cloud Datastore or Bigtable    

[Discussion](/assets/gcp/discussion/3.md)  
[Answer and Vote](/assets/gcp/discussion/3.ans.html)   


# 4

A news feed web service has the following code running on Google App Engine. During peak load, users report that they can see news articles they already viewed.
What is the most likely cause of this problem?          

```python
import news
from flask import Flask, redirect, request
from flask.ext.api import status
from google.appengine.api import users

app = Flask(__name__)
sessions = {}  

@app.route("/")
def homepage():  
    user = users.get_current_user()  
    if not user:  
        return "Invalid login",  
        status.HTTP_401_UNAUTHORIZED

    if user not in sessions:  
        sessions[user] = {"viewed": []}  

    news_articles = news.get_new_news(user, sessions[user]["viewed"])  
    sessions[user]["viewed"] += [n["id"] for n in news_articles]  

    return news.render(news_articles)  

if __name__ == "__main__":  
    app.run()   
```  
  
A. The session variable is local to just a single instance  
B. The session variable is being overwritten in Cloud Datastore  
C. The URL of the API needs to be modified to prevent caching  
D. The HTTP Expires header needs to be set to -1 stop caching  

[Discussion](/assets/gcp/discussion/4.md)   
[Answer and Vote](/assets/gcp/discussion/4.ans.html)   


# 5

An application development team believes their current logging tool will not meet their needs for their new cloud-based product. They want a better tool to capture errors and help them analyze their historical log data. You want to help them find a solution that meets their needs.
What should you do?          

A. Direct them to download and install the Google StackDriver logging agent  
B. Send them a list of online resources about logging best practices  
C. Help them define their requirements and assess viable logging tools  
D. Help them upgrade their current tool to take advantage of any new features  

[Discussion](/assets/gcp/discussion/5.md)   
[Answer and Vote](/assets/gcp/discussion/5.ans.html)   


# 6

You need to reduce the number of unplanned rollbacks of erroneous production deployments in your company's web hosting platform. Improvement to the QA/Test processes accomplished an 80% reduction.  
Which additional two approaches can you take to further reduce the rollbacks?       (Choose two.)    

A. Introduce a green-blue deployment model
B. Replace the QA environment with canary releases
C. Fragment the monolithic platform into microservices
D. Reduce the platform's dependency on relational database systems
E. Replace the platform's relational database systems with a NoSQL database

[Discussion](/assets/gcp/discussion/6.md)   
[Answer and Vote](/assets/gcp/discussion/6.ans.html)   

# 7

To reduce costs, the Director of Engineering has required all developers to move their development infrastructure resources from on-premises virtual machines (VMs) to Google Cloud Platform. These resources go through multiple start/stop events during the day and require state to persist. You have been asked to design the process of running a development environment in Google Cloud while providing cost visibility to the finance department.
Which two steps should you take?       (Choose two.)    

A. Use the - -no-auto-delete flag on all persistent disks and stop the VM  
B. Use the - -auto-delete flag on all persistent disks and terminate the VM  
C. Apply VM CPU utilization label and include it in the BigQuery billing export  
D. Use Google BigQuery billing export and labels to associate cost to groups  
E. Store all state into local SSD, snapshot the persistent disks, and terminate the VM  
F. Store all state in Google Cloud Storage, snapshot the persistent disks, and terminate the VM    

[Discussion](/assets/gcp/discussion/7.md)   
[Answer and Vote](/assets/gcp/discussion/7.ans.html)   


# 8

Your company wants to track whether someone is present in a meeting room reserved for a scheduled meeting. There are 1000 meeting rooms across 5 offices on 3 continents. Each room is equipped with a motion sensor that reports its status every second. The data from the motion detector includes only a sensor ID and several different discrete items of information. Analysts will use this data, together with information about account owners and office locations.  
Which database type should you use?          

A. Flat file  
B. NoSQL  
C. Relational  
D. Blobstore    

[Discussion](/assets/gcp/discussion/8.md)   
[Answer and Vote](/assets/gcp/discussion/8.ans.html)   


# 9

You set up an autoscaling instance group to serve web traffic for an upcoming launch. After configuring the instance group as a backend service to an HTTP(S) load balancer, you notice that virtual machine (VM) instances are being terminated and re-launched every minute. The instances do not have a public IP address.
You have verified the appropriate web response is coming from each instance using the curl command. You want to ensure the backend is configured correctly.
What should you do?        

A. Ensure that a firewall rules exists to allow source traffic on HTTP/HTTPS to reach the load balancer.  
B. Assign a public IP to each instance and configure a firewall rule to allow the load balancer to reach the instance public IP.  
C. Ensure that a firewall rule exists to allow load balancer health checks to reach the instances in the instance group.  
D. Create a tag on each instance with the name of the load balancer. Configure a firewall rule with the name of the load balancer as the source and the instance tag as the destination.    

[Discussion](/assets/gcp/discussion/9.md)   
[Answer and Vote](/assets/gcp/discussion/9.ans.html)   


# 10

You write a Python script to connect to Google BigQuery from a Google Compute Engine virtual machine. The script is printing errors that it cannot connect to BigQuery.  
What should you do to fix the script?          

A. Install the latest BigQuery API client library for Python  
B. Run your script on a new virtual machine with the BigQuery access scope enabled  
C. Create a new service account with BigQuery access and execute your script with that user  
D. Install the bq component for gcloud with the command gcloud components install bq.    


[Discussion](/assets/gcp/discussion/10.md)   
[Answer and Vote](/assets/gcp/discussion/10.ans.html)   


# 11

Your customer is moving an existing corporate application to Google Cloud Platform from an on-premises data center. The business owners require minimal user disruption. There are strict security team requirements for storing passwords.  
What authentication strategy should they use?          

A. Use G Suite Password Sync to replicate passwords into Google  
B. Federate authentication via SAML 2.0 to the existing Identity Provider  
C. Provision users in Google using the Google Cloud Directory Sync tool  
D. Ask users to set their Google password to match their corporate password    

[Discussion](/assets/gcp/discussion/11.md)   
[Answer and Vote](/assets/gcp/discussion/11.ans.html)   


# 12

Your company has successfully migrated to the cloud and wants to analyze their data stream to optimize operations. They do not have any existing code for this analysis, so they are exploring all their options. These options include a mix of batch and stream processing, as they are running some hourly jobs and live-processing some data as it comes in.  
Which technology should they use for this?          

A. Google Cloud Dataproc  
B. Google Cloud Dataflow  
C. Google Container Engine with Bigtable  
D. Google Compute Engine with Google BigQuery    

[Discussion](/assets/gcp/discussion/12.md)   
[Answer and Vote](/assets/gcp/discussion/12.ans.html)   


# 13

Your customer is receiving reports that their recently updated Google App Engine application is taking approximately 30 seconds to load for some of their users.  
This behavior was not reported before the update.  
What strategy should you take?          
  
A. Work with your ISP to diagnose the problem  
B. Open a support ticket to ask for network capture and flow data to diagnose the problem, then roll back your application  
C. Roll back to an earlier known good release initially, then use Stackdriver Trace and Logging to diagnose the problem in a development/test/staging environment  
D. Roll back to an earlier known good release, then push the release again at a quieter period to investigate. Then use Stackdriver Trace and Logging to diagnose the problem  
  
[Discussion](/assets/gcp/discussion/13.md)   
[Answer and Vote](/assets/gcp/discussion/13.ans.html)   


# 14

A production database virtual machine on Google Compute Engine has an ext4-formatted persistent disk for data files. The database is about to run out of storage space.  
How can you remediate the problem with the least amount of downtime?          

A. In the Cloud Platform Console, increase the size of the persistent disk and use the resize2fs command in Linux.  
B. Shut down the virtual machine, use the Cloud Platform Console to increase the persistent disk size, then restart the virtual machine  
C. In the Cloud Platform Console, increase the size of the persistent disk and verify the new space is ready to use with the fdisk command in Linux  
D. In the Cloud Platform Console, create a new persistent disk attached to the virtual machine, format and mount it, and configure the database service to move the files to the new disk  
E. In the Cloud Platform Console, create a snapshot of the persistent disk restore the snapshot to a new larger disk, unmount the old disk, mount the new disk and restart the database service    

[Discussion](/assets/gcp/discussion/14.md)   
[Answer and Vote](/assets/gcp/discussion/14.ans.html)   


# 15

Your application needs to process credit card transactions. You want the smallest scope of Payment Card Industry (PCI) compliance without compromising the ability to analyze transactional data and trends relating to which payment methods are used.
How should you design your architecture?          

A. Create a tokenizer service and store only tokenized data  
B. Create separate projects that only process credit card data  
C. Create separate subnetworks and isolate the components that process credit card data  
D. Streamline the audit discovery phase by labeling all of the virtual machines (VMs) that process PCI data  
E. Enable Logging export to Google BigQuery and use ACLs and views to scope the data shared with the auditor    

[Discussion](/assets/gcp/discussion/15.md)   
[Answer and Vote](/assets/gcp/discussion/15.ans.html)   


# 16
You have been asked to select the storage system for the click-data of your company's large portfolio of websites. This data is streamed in from a custom website analytics package at a typical rate of 6,000 clicks per minute. With bursts of up to 8,500 clicks per second. It must have been stored for future analysis by your data science and user experience teams.
Which storage infrastructure should you choose?        

<details>
  <summary style="cursor: pointer; font-weight: bold; color: #4285f4;">translate</summary>
  <div style="margin-top: 10px; font-family: sans-serif; background: #f9f9f9; padding: 20px; border-radius: 8px; border: 1px solid #ddd; max-width: 600px;">
    <p>您被要求选择用于存储贵公司大量网站点击数据的存储系统。这些数据以每分钟 6,000 次点击的典型速率从自定义网站分析包中流式传输。最高可达每秒 8,500 次点击。这些数据必须已存储以供您的数据科学和用户体验团队将来分析。</p>
  </div>
</details>
    
  
  
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
[Answer and Vote](/assets/gcp/discussion/17.ans.html)   



# 18
Your company is forecasting a sharp increase in the number and size of Apache Spark and Hadoop jobs being run on your local datacenter. You want to utilize the cloud to help you scale this upcoming demand with the least amount of operations work and code change.  
Which product should you use?        

A. Google Cloud Dataflow  
B. Google Cloud Dataproc  
C. Google Compute Engine  
D. Google Kubernetes Engine    

[Discussion](/assets/gcp/discussion/18.md)    
[Answer and Vote](/assets/gcp/discussion/18.ans.html)   


# 19
The database administration team has asked you to help them improve the performance of their new database server running on Google Compute Engine. The database is for importing and normalizing their performance statistics and is built with MySQL running on Debian Linux. They have an n1-standard-8 virtual machine with 80 GB of SSD persistent disk.  
What should they change to get better performance from this system?      

   
A. Increase the virtual machine's memory to 64 GB  
B. Create a new virtual machine running PostgreSQL  
C. Dynamically resize the SSD persistent disk to 500 GB  
D. Migrate their performance metrics warehouse to BigQuery  
E. Modify all of their batch jobs to use bulk inserts into the database    

[Discussion](/assets/gcp/discussion/19.md)    
[Answer and Vote](/assets/gcp/discussion/19.ans.html)   


# 20
You want to optimize the performance of an accurate, real-time, weather-charting application. The data comes from 50,000 sensors sending 10 readings a second, in the format of a timestamp and sensor reading.  
Where should you store the data?        
    

A. Google BigQuery  
B. Google Cloud SQL  
C. Google Cloud Bigtable  
D. Google Cloud Storage    

[Discussion](/assets/gcp/discussion/20.md)    
[Answer and Vote](/assets/gcp/discussion/20.ans.html)   



# 21
Your company's user-feedback portal comprises a standard LAMP stack replicated across two zones. It is deployed in the us-central1 region and uses autoscaled managed instance groups on all layers, except the database. Currently, only a small group of select customers have access to the portal. The portal meets a
99,99% availability SLA under these conditions. However next quarter, your company will be making the portal available to all users, including unauthenticated users. You need to develop a resiliency testing strategy to ensure the system maintains the SLA once they introduce additional user load.  
What should you do?        
     

A. Capture existing users input, and replay captured user load until autoscale is triggered on all layers. At the same time, terminate all resources in one of the zones  
B. Create synthetic random user input, replay synthetic load until autoscale logic is triggered on at least one layer, and introduce ג€chaosג€ to the system by terminating random resources on both zones   
C. Expose the new system to a larger group of users, and increase group size each day until autoscale logic is triggered on all layers. At the same time, terminate random resources on both zones  
D. Capture existing users input, and replay captured user load until resource utilization crosses 80%. Also, derive estimated number of users based on existing user's usage of the app, and deploy enough resources to handle 200% of expected load    

[Discussion](/assets/gcp/discussion/21.md)    
[Answer and Vote](/assets/gcp/discussion/21.ans.html)   



# 22

One of the developers on your team deployed their application in Google Container Engine with the Dockerfile below. They report that their application deployments are taking too long.  
You want to optimize this Dockerfile for faster deployment times without adversely affecting the app's functionality.  

Which two actions should you take?       (Choose two.)  


```bash
FROM ubuntu:16.04    
COPY . /src    
RUN apt-get update && apt-get install -y python python-pip    
RUN pip install -r requirements.txt  
```


A. Remove Python after running pip  
B. Remove dependencies from requirements.txt  
C. Use a slimmed-down base image like Alpine Linux  
D. Use larger machine types for your Google Container Engine node pools  
E. Copy the source after he package dependencies (Python and pip) are installed    

[Discussion](/assets/gcp/discussion/22.md)    
[Answer and Vote](/assets/gcp/discussion/22.ans.html)   



# 23
Your solution is producing performance bugs in production that you did not see in staging and test environments. You want to adjust your test and deployment procedures to avoid this problem in the future.  
What should you do?        

  
A. Deploy fewer changes to production  
B. Deploy smaller changes to production  
C. Increase the load on your test and staging environments   
D. Deploy changes to a small subset of users before rolling out to production    

[Discussion](/assets/gcp/discussion/23.md)    
[Answer and Vote](/assets/gcp/discussion/23.ans.html)   



# 24  
A small number of API requests to your microservices-based application take a very long time. You know that each request to the API can traverse many services.  
You want to know which service takes the longest in those cases.  
What should you do?        
    

A. Set timeouts on your application so that you can fail requests faster  
B. Send custom metrics for each of your requests to Stackdriver Monitoring  
C. Use Stackdriver Monitoring to look for insights that show when your API latencies are high  
D. Instrument your application with Stackdriver Trace in order to break down the request latencies at each microservice    

[Discussion](/assets/gcp/discussion/24.md)  
[Answer and Vote](/assets/gcp/discussion/24.ans.html)   


# 25
During a high traffic portion of the day, one of your relational databases crashes, but the replica is never promoted to a master. You want to avoid this in the future.  
What should you do?        

  
A. Use a different database  
B. Choose larger instances for your database  
C. Create snapshots of your database more regularly  
D. Implement routinely scheduled failovers of your databases

[Discussion](/assets/gcp/discussion/25.md)    
[Answer and Vote](/assets/gcp/discussion/25.ans.html)   


# 26
Your organization requires that metrics from all applications be retained for 5 years for future analysis in possible legal proceedings.
Which approach should you use?        


A. Grant the security team access to the logs in each Project  
B. Configure Stackdriver Monitoring for all Projects, and export to BigQuery  
C. Configure Stackdriver Monitoring for all Projects with the default retention policies  
D. Configure Stackdriver Monitoring for all Projects, and export to Google Cloud Storage    

[Discussion](/assets/gcp/discussion/26.md)  
[Answer and Vote](/assets/gcp/discussion/26.ans.html)   


# 27

Your company has decided to build a backup replica of their on-premises user authentication PostgreSQL database on Google Cloud Platform. The database is 4 TB, and large updates are frequent. Replication requires private address space communication.
Which networking approach should you use?         

A. Google Cloud Dedicated Interconnect  
B. Google Cloud VPN connected to the data center network  
C. A NAT and TLS translation gateway installed on-premises  
D. A Google Compute Engine instance with a VPN server installed connected to the data center network    

[Discussion](/assets/gcp/discussion/27.md)   
[Answer and Vote](/assets/gcp/discussion/27.ans.html)   
[A & B html](/assets/gcp/discussion/27.vs.html)  

# 28

Auditors visit your teams every 12 months and ask to review all the Google Cloud Identity and Access Management (Cloud IAM) policy changes in the previous 12 months. You want to streamline and expedite the analysis and audit process.  
What should you do?        
   

A. Create custom Google Stackdriver alerts and send them to the auditor  
B. Enable Logging export to Google BigQuery and use ACLs and views to scope the data shared with the auditor  
C. Use cloud functions to transfer log entries to Google Cloud SQL and use ACLs and views to limit an auditor's view  
D. Enable Google Cloud Storage (GCS) log export to audit logs into a GCS bucket and delegate access to the bucket    

[Discussion](/assets/gcp/discussion/28.md)  
[Answer and Vote](/assets/gcp/discussion/28.ans.html)   


# 29
You are designing a large distributed application with 30 microservices. Each of your distributed microservices needs to connect to a database back-end. You want to store the credentials securely.  
Where should you store the credentials?        
  

A. In the source code  
B. In an environment variable  
C. In a secret management system  
D. In a config file that has restricted access through ACLs    

[Discussion](/assets/gcp/discussion/29.md)    
[Answer and Vote](/assets/gcp/discussion/29.ans.html)   


# 30

A lead engineer wrote a custom tool that deploys virtual machines in the legacy data center. He wants to migrate the custom tool to the new cloud environment.  
You want to advocate for the adoption of Google Cloud Deployment Manager.  
What are two business risks of migrating to Cloud Deployment Manager?       (Choose two.)      

A. Cloud Deployment Manager uses Python  
B. Cloud Deployment Manager APIs could be deprecated in the future  
C. Cloud Deployment Manager is unfamiliar to the company's engineers  
D. Cloud Deployment Manager requires a Google APIs service account to run  
E. Cloud Deployment Manager can be used to permanently delete cloud resources  
F. Cloud Deployment Manager only supports automation of Google Cloud resources    

[Discussion](/assets/gcp/discussion/30.md)  
[Answer](/assets/gcp/discussion/30.ans.html)  

# 31

A development manager is building a new application. He asks you to review his requirements and identify what cloud technologies he can use to meet them. The application must:  
1. Be based on open-source technology for cloud portability  
2. Dynamically scale compute capacity based on demand  
3. Support continuous software delivery  
4. Run multiple segregated copies of the same application stack  
5. Deploy application bundles using dynamic templates  
6. Route network traffic to specific services based on URL  
Which combination of technologies will meet all of his requirements?          
  

A. Google Kubernetes Engine, Jenkins, and Helm    
B. Google Kubernetes Engine and Cloud Load Balancing  
C. Google Kubernetes Engine and Cloud Deployment Manager  
D. Google Kubernetes Engine, Jenkins, and Cloud Load Balancing    

[Discussion](/assets/gcp/discussion/31.md)    
[Answer](/assets/gcp/discussion/31.ans.html)  


# 32

You have created several pre-emptible Linux virtual machine instances using Google Compute Engine. You want to properly shut down your application before the virtual machines are preempted.  
What should you do?        

A. Create a shutdown script named k99.shutdown in the /etc/rc.6.d/ directory  
B. Create a shutdown script registered as a xinetd service in Linux and configure a Stackdriver endpoint check to call the service  
C. Create a shutdown script and use it as the value for a new metadata entry with the key shutdown-script in the Cloud Platform Console when you create the new virtual machine instance  
D. Create a shutdown script, registered as a xinetd service in Linux, and use the gcloud compute instances add-metadata command to specify the service URL as the value for a new metadata entry with the key shutdown-script-url    

[Discussion](/assets/gcp/discussion/32.md)    
[Answer](/assets/gcp/discussion/32.ans.html)  


# 33

Your organization has a 3-tier web application deployed in the same network on Google Cloud Platform. Each tier (web, API, and database) scales independently of the others. Network traffic should flow through the web to the API tier and then on to the database tier. Traffic should not flow between the web and the database tier.  
How should you configure the network?           

A. Add each tier to a different subnetwork  
B. Set up software based firewalls on individual VMs  
C. Add tags to each tier and set up routes to allow the desired traffic flow  
D. Add tags to each tier and set up firewall rules to allow the desired traffic flow    

[Discussion](/assets/gcp/discussion/33.md)    
[Answer](/assets/gcp/discussion/33.ans.html)  


# 34

Your development team has installed a new Linux kernel module on the batch servers in Google Compute Engine (GCE) virtual machines (VMs) to speed up the nightly batch process. Two days after the installation, 50% of the batch servers failed the nightly batch run. You want to collect details on the failure to pass back to the development team.  
Which three actions should you take?       (Choose three.)   


A. Use Stackdriver Logging to search for the module log entries  
B. Read the debug GCE Activity log using the API or Cloud Console  
C. Use gcloud or Cloud Console to connect to the serial console and observe the logs  
D. Identify whether a live migration event of the failed server occurred, using in the activity log  
E. Adjust the Google Stackdriver timeline to match the failure time, and observe the batch server metrics  
F. Export a debug VM into an image, and run the image on a local server where kernel log messages will be displayed on the native screen    

[Discussion](/assets/gcp/discussion/34.md)    
[Answer](/assets/gcp/discussion/34.ans.html)    

# 35
Your company wants to try out the cloud with low risk. They want to archive approximately 100 TB of their log data to the cloud and test the analytics features available to them there, while also retaining that data as a long-term disaster recovery backup.  
Which two steps should you take?       (Choose two.)     

A. Load logs into Google BigQuery  
B. Load logs into Google Cloud SQL  
C. Import logs into Google Stackdriver  
D. Insert logs into Google Cloud Bigtable  
E. Upload log files into Google Cloud Storage    

[Discussion](/assets/gcp/discussion/35.md)  
[Answer](/assets/gcp/discussion/35.ans.html)    


# 36

You created a pipeline that can deploy your source code changes to your infrastructure in instance groups for self-healing. One of the changes negatively affects your key performance indicator. You are not sure how to fix it, and investigation could take up to a week.  
What should you do?          

A. Log in to a server, and iterate on the fox locally  
B. Revert the source code change, and rerun the deployment pipeline  
C. Log into the servers with the bad code change, and swap in the previous code  
D. Change the instance group template to the previous one, and delete all instances       

[Discussion](/assets/gcp/discussion/36.md)  
[Answer](/assets/gcp/discussion/36.ans.html)    


# 37

Your organization wants to control IAM policies for different departments independently, but centrally.  
Which approach should you take?          

A. Multiple Organizations with multiple Folders  
B. Multiple Organizations, one for each department  
C. A single Organization with Folders for each department  
D. A single Organization with multiple projects, each with a central owner       

[Discussion](/assets/gcp/discussion/37.md)  
[Answers and Votes](/assets/gcp/discussion/37.ans.html)    



# 38 

You deploy your custom Java application to Google App Engine. It fails to deploy and gives you the following stack trace.  
What should you do?          

A. Upload missing JAR files and redeploy your application.  
B. Digitally sign all of your JAR files and redeploy your application  
C. Recompile the CLoakedServlet class using and MD5 hash instead of SHA1    

[Discussion](/assets/gcp/discussion/38.md)  
[Answer](/assets/gcp/discussion/38.ans.html)    


# 39

You are designing a mobile chat application. You want to ensure people cannot spoof chat messages, by providing a message were sent by a specific user.
What should you do?          

A. Tag messages client side with the originating user identifier and the destination user.  
B. Encrypt the message client side using block-based encryption with a shared key.  
C. Use public key infrastructure (PKI) to encrypt the message client side using the originating user's private key.  
D. Use a trusted certificate authority to enable SSL connectivity between the client application and the server.    
 

[Discussion](/assets/gcp/discussion/39.md)  
[Answer](/assets/gcp/discussion/39.ans.html)    


# 40
As part of implementing their disaster recovery plan, your company is trying to replicate their production MySQL database from their private data center to their GCP project using a Google Cloud VPN connection. They are experiencing latency issues and a small amount of packet loss that is disrupting the replication.  
What should they do?        

A. Configure their replication to use UDP.  
B. Configure a Google Cloud Dedicated Interconnect.  
C. Restore their database daily using Google Cloud SQL.  
D. Add additional VPN connections and load balance them.  
E. Send the replicated transaction to Google Cloud Pub/Sub.       

[Discussion](/assets/gcp/discussion/40.md)  
[Answer](/assets/gcp/discussion/40.ans.html)    


# 41

Your customer support tool logs all email and chat conversations to Cloud Bigtable for retention and analysis. What is the recommended approach for sanitizing this data of personally identifiable information or payment card information before initial storage?          

A. Hash all data using SHA256  
B. Encrypt all data using elliptic curve cryptography  
C. De-identify the data with the Cloud Data Loss Prevention API  
D. Use regular expressions to find and redact phone numbers, email addresses, and credit card numbers     

[Discussion](/assets/gcp/discussion/41.md)  
[Answer](/assets/gcp/discussion/41.ans.html)    


# 42

You are using Cloud Shell and need to install a custom utility for use in a few weeks. Where can you store the file so it is in the default execution path and persists across sessions?          

A. ~/bin  
B. Cloud Storage  
C. /google/scripts  
D. /usr/local/bin    

[Discussion](/assets/gcp/discussion/42.md)  
[Answer](/assets/gcp/discussion/42.ans.html)    


# 43

You want to create a private connection between your instances on Compute Engine and your on-premises data center. You require a connection of at least 20
Gbps. You want to follow Google-recommended practices. How should you set up the connection?          

A. Create a VPC and connect it to your on-premises data center using Dedicated Interconnect.  
B. Create a VPC and connect it to your on-premises data center using a single Cloud VPN.  
C. Create a Cloud Content Delivery Network (Cloud CDN) and connect it to your on-premises data center using Dedicated Interconnect.  
D. Create a Cloud Content Delivery Network (Cloud CDN) and connect it to your on-premises datacenter using a single Cloud VPN.        

[Discussion](/assets/gcp/discussion/43.md)  
[Answer](/assets/gcp/discussion/43.ans.html)    


# 44

You are analyzing and defining business processes to support your startup's trial usage of GCP, and you don't yet know what consumer demand for your product will be. Your manager requires you to minimize GCP service costs and adhere to Google best practices. What should you do?          

A. Utilize free tier and sustained use discounts. Provision a staff position for service cost management.  
B. Utilize free tier and sustained use discounts. Provide training to the team about service cost management.  
C. Utilize free tier and committed use discounts. Provision a staff position for service cost management.  
D. Utilize free tier and committed use discounts. Provide training to the team about service cost management.     


[Discussion](/assets/gcp/discussion/44.md)  
[Answer](/assets/gcp/discussion/44.ans.html)    


# 45

You are building a continuous deployment pipeline for a project stored in a Git source repository and want to ensure that code changes can be verified before deploying to production. What should you do?          

A. Use Spinnaker to deploy builds to production using the red/black deployment strategy so that changes can easily be rolled back.  
B. Use Spinnaker to deploy builds to production and run tests on production deployments.  
C. Use Jenkins to build the staging branches and the master branch. Build and deploy changes to production for 10% of users before doing a complete rollout.  
D. Use Jenkins to monitor tags in the repository. Deploy staging tags to a staging environment for testing. After testing, tag the repository for production and deploy that to the production environment.    

[Discussion](/assets/gcp/discussion/45.md)  
[Answer](/assets/gcp/discussion/45.ans.html)    


# 46

You have an outage in your Compute Engine managed instance group: all instances keep restarting after 5 seconds. You have a health check configured, but autoscaling is disabled. Your colleague, who is a Linux expert, offered to look into the issue. You need to make sure that he can access the VMs. What should you do?          

A. Grant your colleague the IAM role of project Viewer  
B. Perform a rolling restart on the instance group  
C. Disable the health check for the instance group. Add his SSH key to the project-wide SSH Keys  
D. Disable autoscaling for the instance group. Add his SSH key to the project-wide SSH Keys      

[Discussion](/assets/gcp/discussion/46.md)  
[Answer](/assets/gcp/discussion/46.ans.html)    


# 47
Your company is migrating its on-premises data center into the cloud. As part of the migration, you want to integrate Google Kubernetes Engine (GKE) for workload orchestration. Parts of your architecture must also be PCI DSS-compliant. Which of the following is most accurate?          

A. App Engine is the only compute platform on GCP that is certified for PCI DSS hosting.  
B. GKE cannot be used under PCI DSS because it is considered shared hosting.  
C. GKE and GCP provide the tools you need to build a PCI DSS-compliant environment.  
D. All Google Cloud services are usable because Google Cloud Platform is certified PCI-compliant.       

[Discussion](/assets/gcp/discussion/47.md)  
[Answer](/assets/gcp/discussion/47.ans.html)    


# 48
Your company has multiple on-premises systems that serve as sources for reporting. The data has not been maintained well and has become degraded over time.
You want to use Google-recommended practices to detect anomalies in your company data. What should you do?          

A. Upload your files into Cloud Storage. Use Cloud Datalab to explore and clean your data.  
B. Upload your files into Cloud Storage. Use Cloud Dataprep to explore and clean your data.  
C. Connect Cloud Datalab to your on-premises systems. Use Cloud Datalab to explore and clean your data.  
D. Connect Cloud Dataprep to your on-premises systems. Use Cloud Dataprep to explore and clean your data.      

[Discussion](/assets/gcp/discussion/48.md)  
[Answer and Vote](/assets/gcp/discussion/48.ans.html)  


# 49
Google Cloud Platform resources are managed hierarchically using organization, folders, and projects. When Cloud Identity and Access Management (IAM) policies exist at these different levels, what is the effective policy at a particular node of the hierarchy?          

A. The effective policy is determined only by the policy set at the node  
B. The effective policy is the policy set at the node and restricted by the policies of its ancestors  
C. The effective policy is the union of the policy set at the node and policies inherited from its ancestors  
D. The effective policy is the intersection of the policy set at the node and policies inherited from its ancestors       

[Discussion](/assets/gcp/discussion/49.md)  
[Answer and Vote](/assets/gcp/discussion/49.ans.html)  


# 50

You are migrating your on-premises solution to Google Cloud in several phases. You will use Cloud VPN to maintain a connection between your on-premises systems and Google Cloud until the migration is completed. You want to make sure all your on-premise systems remain reachable during this period. How should you organize your networking in Google Cloud?          

A. Use the same IP range on Google Cloud as you use on-premises  
B. Use the same IP range on Google Cloud as you use on-premises for your primary IP range and use a secondary range that does not overlap with the range you use on-premises  
C. Use an IP range on Google Cloud that does not overlap with the range you use on-premises  
D. Use an IP range on Google Cloud that does not overlap with the range you use on-premises for your primary IP range and use a secondary range with the same IP range as you use on-premises      


[Discussion](/assets/gcp/discussion/50.md)  
[Answer and Vote](/assets/gcp/discussion/50.ans.html)  

