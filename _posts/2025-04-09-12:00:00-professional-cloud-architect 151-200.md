---
layout: home
title: "professional cloud architect"
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

A. 1. Use Linux shasum to compute a digest of files you want to upload. 2. Use gsutil -m to upload all the files to Cloud Storage. 3. Use gsutil cp to download the uploaded files. 4. Use Linux shasum to compute a digest of the downloaded files. 5. Compare the hashes.  
B. 1. Use gsutil -m to upload the files to Cloud Storage. 2. Develop a custom Java application that computes CRC32C hashes. 3. Use gsutil ls -L gs://[YOUR_BUCKET_NAME] to collect CRC32C hashes of the uploaded files. 4. Compare the hashes.  
C. 1. Use gsutil -m to upload all the files to Cloud Storage. 2. Use gsutil cp to download the uploaded files. 3. Use Linux diff to compare the content of the files.  
D. 1. Use gsutil -m to upload the files to Cloud Storage. 2. Use gsutil hash -c FILE_NAME to generate CRC32C hashes of all on-premises files. 3. Use gsutil ls -L gs://[YOUR_BUCKET_NAME] to collect CRC32C hashes of the uploaded files. 4. Compare the hashes.  

[Discussion](/assets/gcp/discussion/152.md)

# 153

You have deployed an application on Anthos clusters (formerly Anthos GKE). According to the SRE practices at your company, you need to be alerted if request latency is above a certain threshold for a specified amount of time. What should you do?  

A. Install Anthos Service Mesh on your cluster. Use the Google Cloud Console to define a Service Level Objective (SLO), and create an alerting policy based on this SLO.  
B. Enable the Cloud Trace API on your project, and use Cloud Monitoring Alerts to send an alert based on the Cloud Trace metrics.   
C. Use Cloud Profiler to follow up the request latency. Create a custom metric in Cloud Monitoring based on the results of Cloud Profiler, and create an Alerting policy in case this metric exceeds the threshold.  
D. Configure Anthos Config Management on your cluster, and create a yaml file that defines the SLO and alerting policy you want to deploy in your cluster.  

[Discussion](/assets/gcp/discussion/153.md)

# 154

Your company has a stateless web API that performs scientific calculations. The web API runs on a single Google Kubernetes Engine (GKE) cluster. The cluster is currently deployed in us-central1. Your company has expanded to offer your API to customers in Asia. You want to reduce the latency for users in Asia.  
What should you do?   

A. Create a second GKE cluster in asia-southeast1, and expose both APIs using a Service of type LoadBalancer. Add the public IPs to the Cloud DNS zone.  
B. Use a global HTTP(s) load balancer with Cloud CDN enabled.  
C. Create a second GKE cluster in asia-southeast1, and use kubemci to create a global HTTP(s) load balancer.  
D. Increase the memory and CPU allocated to the application in the cluster.  


[Discussion](/assets/gcp/discussion/154.md)

# 155

You are migrating third-party applications from optimized on-premises virtual machines to Google Cloud. You are unsure about the optimum CPU and memory options. The applications have a consistent usage pattern across multiple weeks. You want to optimize resource usage for the lowest cost. What should you do?  

A. Create an instance template with the smallest available machine type, and use an image of the third-party application taken from a current on-premises virtual machine. Create a managed instance group that uses average CPU utilization to autoscale the number of instances in the group. Modify the average CPU utilization threshold to optimize the number of instances running.  
B. Create an App Engine flexible environment, and deploy the third-party application using a Dockerfile and a custom runtime. Set CPU and memory options similar to your application's current on-premises virtual machine in the app.yaml file.  
C. Create multiple Compute Engine instances with varying CPU and memory options. Install the Cloud Monitoring agent, and deploy the third-party application on each of them. Run a load test with high traffic levels on the application, and use the results to determine the optimal settings.  
D. Create a Compute Engine instance with CPU and memory options similar to your application's current on-premises virtual machine. Install the Cloud Monitoring agent, and deploy the third-party application. Run a load test with normal traffic levels on the application, and follow the Rightsizing Recommendations in the Cloud Console.  

[Discussion](/assets/gcp/discussion/155.md)

# 156

[Discussion](/assets/gcp/discussion/156.md)

# 157

[Discussion](/assets/gcp/discussion/157.md)

# 158

[Discussion](/assets/gcp/discussion/158.md)

# 159

[Discussion](/assets/gcp/discussion/159.md)

# 160

[Discussion](/assets/gcp/discussion/160.md)

# 161

[Discussion](/assets/gcp/discussion/161.md)

# 162

[Discussion](/assets/gcp/discussion/162.md)

# 163

[Discussion](/assets/gcp/discussion/163.md)

# 164

[Discussion](/assets/gcp/discussion/164.md)

# 165

[Discussion](/assets/gcp/discussion/165.md)

# 166

[Discussion](/assets/gcp/discussion/166.md)

# 167

[Discussion](/assets/gcp/discussion/167.md)

# 168

[Discussion](/assets/gcp/discussion/168.md)

# 169

[Discussion](/assets/gcp/discussion/169.md)

# 170

[Discussion](/assets/gcp/discussion/170.md)

# 171

[Discussion](/assets/gcp/discussion/171.md)

# 172

[Discussion](/assets/gcp/discussion/172.md)

# 173

[Discussion](/assets/gcp/discussion/173.md)

# 174

[Discussion](/assets/gcp/discussion/174.md)

# 175

[Discussion](/assets/gcp/discussion/175.md)

# 176

[Discussion](/assets/gcp/discussion/176.md)

# 177

[Discussion](/assets/gcp/discussion/177.md)

# 178

[Discussion](/assets/gcp/discussion/178.md)

# 179

[Discussion](/assets/gcp/discussion/179.md)

# 180

[Discussion](/assets/gcp/discussion/180.md)

# 181

[Discussion](/assets/gcp/discussion/181.md)

# 182

[Discussion](/assets/gcp/discussion/182.md)

# 183

[Discussion](/assets/gcp/discussion/183.md)

# 184

[Discussion](/assets/gcp/discussion/184.md)

# 185

[Discussion](/assets/gcp/discussion/185.md)

# 186

[Discussion](/assets/gcp/discussion/186.md)

# 187

[Discussion](/assets/gcp/discussion/187.md)

# 188

[Discussion](/assets/gcp/discussion/188.md)

# 189

[Discussion](/assets/gcp/discussion/189.md)

# 190

[Discussion](/assets/gcp/discussion/190.md)

# 191

[Discussion](/assets/gcp/discussion/191.md)

# 192

[Discussion](/assets/gcp/discussion/192.md)

# 193

[Discussion](/assets/gcp/discussion/193.md)

# 194

[Discussion](/assets/gcp/discussion/194.md)

# 195

[Discussion](/assets/gcp/discussion/195.md)

# 196

[Discussion](/assets/gcp/discussion/196.md)

# 197

[Discussion](/assets/gcp/discussion/197.md)

# 198

[Discussion](/assets/gcp/discussion/198.md)

# 199

[Discussion](/assets/gcp/discussion/199.md)

# 200

[Discussion](/assets/gcp/discussion/200.md)
