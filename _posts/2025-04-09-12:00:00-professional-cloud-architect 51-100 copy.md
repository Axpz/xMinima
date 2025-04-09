---
layout: home
title: "professional cloud architect"
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

您在 App Engine 应用中发现了一个由 Cloud Datastore 索引缺失导致的错误。您已创建包含所需索引的 YAML 文件，并希望将这些新索引部署到 Cloud Datastore。您应该怎么做？

A. 将 gcloud datastore create-indexes 指向您的配置文件  
B. 将配置文件上传到 App Engine 的默认 Cloud Storage 存储桶，并让 App Engine 检测新的索引  
C. 在 GCP Console 中，使用 Datastore Admin 删除当前索引并上传新的配置文件  
D. 创建一个 HTTP 请求到内置 Python 模块，将索引配置文件发送到您的应用程序  


[Discussion](/assets/gcp/discussion/51.md)

# 52

You have an application that will run on Compute Engine. You need to design an architecture that takes into account a disaster recovery plan that requires your application to fail over to another region in case of a regional outage. What should you do?  

A. Deploy the application on two Compute Engine instances in the same project but in a different region. Use the first instance to serve traffic, and use the HTTP load balancing service to fail over to the standby instance in case of a disaster.  
B. Deploy the application on a Compute Engine instance. Use the instance to serve traffic, and use the HTTP load balancing service to fail over to an instance on your premises in case of a disaster.  
C. Deploy the application on two Compute Engine instance groups, each in the same project but in a different region. Use the first instance group to serve traffic, and use the HTTP load balancing service to fail over to the standby instance group in case of a disaster.  
D. Deploy the application on two Compute Engine instance groups, each in a separate project and a different region. Use the first instance group to serve traffic, and use the HTTP load balancing service to fail over to the standby instance group in case of a disaster.  

您有一个将在 Compute Engine 上运行的应用。您需要设计一个架构，其中要考虑灾难恢复计划，该计划要求您的应用在发生区域性服务中断时故障转移到另一个区域。您应该怎么做？

A. 在同一项目但不同区域的两个 Compute Engine 实例上部署应用程序。使用第一个实例来处理流量，并使用 HTTP 负载平衡服务在发生灾难时故障转移到备用实例。  
B. 在 Compute Engine 实例上部署应用程序。使用该实例来处理流量，并在发生灾难时使用 HTTP 负载均衡服务将故障转移到您本地的实例。  
C. 将应用程序部署在两个 Compute Engine 实例组上，每个实例组位于同一个项目，但位于不同的区域。使用第一个实例组来处理流量，并使用 HTTP 负载均衡服务在发生灾难时故障转移到备用实例组。  
D. 在两个 Compute Engine 实例组上部署应用程序，每个实例组位于不同的项目和不同的区域。使用第一个实例组来处理流量，并使用 HTTP 负载平衡服务在发生灾难时故障转移到备用实例组。  

[Discussion](/assets/gcp/discussion/52.md)

# 53

You are deploying an application on App Engine that needs to integrate with an on-premises database. For security purposes, your on-premises database must not be accessible through the public internet. What should you do?

A. Deploy your application on App Engine standard environment and use App Engine firewall rules to limit access to the open on-premises database.  
B. Deploy your application on App Engine standard environment and use Cloud VPN to limit access to the on-premises database.  
C. Deploy your application on App Engine flexible environment and use App Engine firewall rules to limit access to the on-premises database.  
D. Deploy your application on App Engine flexible environment and use Cloud VPN to limit access to the on-premises database.  

[Discussion](/assets/gcp/discussion/53.md)

# 54

You are working in a highly secured environment where public Internet access from the Compute Engine VMs is not allowed. You do not yet have a VPN connection to access an on-premises file server. You need to install specific software on a Compute Engine instance. How should you install the software?

A. Upload the required installation files to Cloud Storage. Configure the VM on a subnet with a Private Google Access subnet. Assign only an internal IP address to the VM. Download the installation files to the VM using gsutil.  
B. Upload the required installation files to Cloud Storage and use firewall rules to block all traffic except the IP address range for Cloud Storage. Download the files to the VM using gsutil.  
C. Upload the required installation files to Cloud Source Repositories. Configure the VM on a subnet with a Private Google Access subnet. Assign only an internal IP address to the VM. Download the installation files to the VM using gcloud.  
D. Upload the required installation files to Cloud Source Repositories and use firewall rules to block all traffic except the IP address range for Cloud Source Repositories. Download the files to the VM using gsutil.  

您在高度安全的环境中工作，不允许从 Compute Engine VM 进行公共互联网访问。您尚未建立 VPN 连接来访问本地文件服务器。您需要在 Compute Engine 实例上安装特定软件。您应该如何安装该软件？

A. 将所需的安装文件上传到 Cloud Storage。在具有私有 Google Access 子网的子网上配置虚拟机。仅为虚拟机分配一个内部 IP 地址。使用 gsutil 将安装文件下载到虚拟机。  
B. 将所需的安装文件上传到云存储，并使用防火墙规则阻止除云存储 IP 地址范围之外的所有流量。使用 gsutil 将文件下载到虚拟机。  
C. 将所需的安装文件上传到 Cloud Source Repositories。在具有私有 Google Access 子网的子网上配置虚拟机。仅为虚拟机分配一个内部 IP 地址。使用 gcloud 将安装文件下载到虚拟机。  
D. 将所需的安装文件上传到 Cloud Source Repositories，并使用防火墙规则阻止除 Cloud Source Repositories 的 IP 地址范围之外的所有流量。使用 gsutil 将文件下载到虚拟机。  

[Discussion](/assets/gcp/discussion/54.md)

# 55

Your company is moving 75 TB of data into Google Cloud. You want to use Cloud Storage and follow Google-recommended practices. What should you do?  
贵公司正在将 75 TB 的数据迁移到 Google Cloud。您希望使用 Cloud Storage 并遵循 Google 推荐的做法。您应该怎么做？  

A. Move your data onto a Transfer Appliance. Use a Transfer Appliance Rehydrator to decrypt the data into Cloud Storage.  
B. Move your data onto a Transfer Appliance. Use Cloud Dataprep to decrypt the data into Cloud Storage.  
C. Install gsutil on each server that contains data. Use resumable transfers to upload the data into Cloud Storage.  
D. Install gsutil on each server containing data. Use streaming transfers to upload the data into Cloud Storage.  

[Discussion](/assets/gcp/discussion/55.md)

# 56

You have an application deployed on Google Kubernetes Engine using a Deployment named echo-deployment. The deployment is exposed using a Service called echo-service. You need to perform an update to the application with minimal downtime to the application. What should you do?  

您在 Google Kubernetes Engine 上部署了一个应用程序，部署名为 echo-deployment。该部署通过名为 echo-service 的服务进行公开。您需要在最大程度地减少应用程序停机时间的情况下对该应用程序进行更新。您应该怎么做？  

A. Use kubectl set image deployment/echo-deployment <new-image>  
B. Use the rolling update functionality of the Instance Group behind the Kubernetes cluster  
C. Update the deployment yaml file with the new container image. Use kubectl delete deployment/echo-deployment and kubectl create ג€"f <yaml-file>  
D. Update the service yaml file which the new container image. Use kubectl delete service/echo-service and kubectl create ג€"f <yaml-file>  

[Discussion](/assets/gcp/discussion/56.md)

# 57

Your company is using BigQuery as its enterprise data warehouse. Data is distributed over several Google Cloud projects. All queries on BigQuery need to be billed on a single project. You want to make sure that no query costs are incurred on the projects that contain the data. Users should be able to query the datasets, but not edit them.  
How should you configure users' access roles?  
您的公司正在使用 BigQuery 作为其企业数据仓库。数据分布在多个 Google Cloud 项目中。BigQuery 上的所有查询都需要在单个项目上计费。您希望确保包含这些数据的项目不会产生任何查询费用。用户应该能够查询数据集，但不能编辑它们。  
您应该如何配置用户的访问角色？  

A. Add all users to a group. Grant the group the role of BigQuery user on the billing project and BigQuery dataViewer on the projects that contain the data.  
B. Add all users to a group. Grant the group the roles of BigQuery dataViewer on the billing project and BigQuery user on the projects that contain the data.  
C. Add all users to a group. Grant the group the roles of BigQuery jobUser on the billing project and BigQuery dataViewer on the projects that contain the data.  
D. Add all users to a group. Grant the group the roles of BigQuery dataViewer on the billing project and BigQuery jobUser on the projects that contain the data.  

[Discussion](/assets/gcp/discussion/57.md)

# 58

You have developed an application using Cloud ML Engine that recognizes famous paintings from uploaded images. You want to test the application and allow specific people to upload images for the next 24 hours. Not all users have a Google Account. How should you have users upload images?  
您使用 Cloud ML Engine 开发了一款应用，可以从上传的图片中识别名画。您想测试该应用，并允许特定用户在接下来的 24 小时内上传图片。并非所有用户都拥有 Google 帐户。您应该如何让用户上传图片？


A. Have users upload the images to Cloud Storage. Protect the bucket with a password that expires after 24 hours.  
B. Have users upload the images to Cloud Storage using a signed URL that expires after 24 hours.  
C. Create an App Engine web application where users can upload images. Configure App Engine to disable the application after 24 hours. Authenticate users via Cloud Identity.  
D. Create an App Engine web application where users can upload images for the next 24 hours. Authenticate users via Cloud Identity.  


[Discussion](/assets/gcp/discussion/58.md)

# 59

Your web application must comply with the requirements of the European Union's General Data Protection Regulation (GDPR). You are responsible for the technical architecture of your web application. What should you do?  
您的 Web 应用程序必须符合欧盟《通用数据保护条例》(GDPR) 的要求。您负责 Web 应用程序的技术架构。您应该怎么做？


A. Ensure that your web application only uses native features and services of Google Cloud Platform, because Google already has various certifications and provides ג€pass-onג€ compliance when you use native features.  
B. Enable the relevant GDPR compliance setting within the GCPConsole for each of the services in use within your application.  
C. Ensure that Cloud Security Scanner is part of your test planning strategy in order to pick up any compliance gaps.  
D. Define a design for the security of data in your web application that meets GDPR requirements.  定义符合 GDPR 要求的 Web 应用程序中数据安全性的设计。


[Discussion](/assets/gcp/discussion/59.md)

# 60

You need to set up Microsoft SQL Server on GCP. Management requires that there's no downtime in case of a data center outage in any of the zones within a
GCP region. What should you do?  
您需要在 GCP 上设置 Microsoft SQL Server。管理层要求，即使
GCP 区域内任何可用区的数据中心发生故障，也不会造成停机。您应该怎么做？  

A. Configure a Cloud SQL instance with high availability enabled.  
B. Configure a Cloud Spanner instance with a regional instance configuration.  
C. Set up SQL Server on Compute Engine, using Always On Availability Groups using Windows Failover Clustering. Place nodes in different subnets.  
D. Set up SQL Server Always On Availability Groups using Windows Failover Clustering. Place nodes in different zones.  

[Discussion](/assets/gcp/discussion/60.md)

# 61

The development team has provided you with a Kubernetes Deployment file. You have no infrastructure yet and need to deploy the application. What should you do?
开发团队已经为您提供了 Kubernetes 部署文件。您还没有基础设施，需要部署应用程序。您应该怎么做？

A. Use gcloud to create a Kubernetes cluster. Use Deployment Manager to create the deployment.   
B. Use gcloud to create a Kubernetes cluster. Use kubectl to create the deployment.  
C. Use kubectl to create a Kubernetes cluster. Use Deployment Manager to create the deployment.  
D. Use kubectl to create a Kubernetes cluster. Use kubectl to create the deployment.  

[Discussion](/assets/gcp/discussion/61.md)

# 62

You need to evaluate your team readiness for a new GCP project. You must perform the evaluation and create a skills gap plan which incorporates the business goal of cost optimization. Your team has deployed two GCP projects successfully to date. What should you do?  
您需要评估团队对新 GCP 项目的准备情况。您必须进行评估并制定技能差距计划，其中要包含成本优化这一业务目标。到目前为止，您的团队已经成功部署了两个 GCP 项目。您应该怎么做？

A. Allocate budget for team training. Set a deadline for the new GCP project.  
B. Allocate budget for team training. Create a roadmap for your team to achieve Google Cloud certification based on job role.  
C. Allocate budget to hire skilled external consultants. Set a deadline for the new GCP project.  
D. Allocate budget to hire skilled external consultants. Create a roadmap for your team to achieve Google Cloud certification based on job role.  

[Discussion](/assets/gcp/discussion/62.md)

# 63

You are designing an application for use only during business hours. For the minimum viable product release, you'd like to use a managed product that automatically `scales to zero` so you don't incur costs when there is no activity.  
Which primary compute resource should you choose?  
您正在设计一款仅在工作时间使用的应用程序。对于最小可行产品版本，您希望使用一款能够自动“缩容至零”的托管产品，以便在没有活动时避免产生成本。  
您应该选择哪种主要计算资源？  

A. Cloud Functions  
B. Compute Engine  
C. Google Kubernetes Engine  
D. AppEngine flexible environment  

[Discussion](/assets/gcp/discussion/63.md)

# 64

You are creating an App Engine application that uses Cloud Datastore as its persistence layer. You need to retrieve several root entities for which you have the identifiers. You want to minimize the overhead in operations performed by Cloud Datastore. What should you do?  
您正在创建一个使用 Cloud Datastore 作为持久层的 App Engine 应用。您需要检索多个拥有标识符的根实体。您希望最大限度地减少 Cloud Datastore 执行的操作开销。您应该怎么做？  

A. Create the Key object for each Entity and run a batch get operation  
B. Create the Key object for each Entity and run multiple get operations, one operation for each entity  
C. Use the identifiers to create a query filter and run a batch query operation  
D. Use the identifiers to create a query filter and run multiple query operations, one operation for each entity  

[Discussion](/assets/gcp/discussion/64.md)

# 65

You need to upload files from your on-premises environment to Cloud Storage. You want the files to be encrypted on Cloud Storage using customer-supplied encryption keys. What should you do?  
您需要将文件从本地环境上传到 Cloud Storage。您希望使用客户提供的加密密钥在 Cloud Storage 上对这些文件进行加密。您应该怎么做？  

A. Supply the encryption key in a .boto configuration file. Use gsutil to upload the files.  
B. Supply the encryption key using gcloud config. Use gsutil to upload the files to that bucket.  
C. Use gsutil to upload the files, and use the flag --encryption-key to supply the encryption key.  
D. Use gsutil to create a bucket, and use the flag --encryption-key to supply the encryption key. Use gsutil to upload the files to that bucket.  

[Discussion](/assets/gcp/discussion/65.md)

# 66

Your customer wants to capture multiple GBs of aggregate real-time key performance indicators (KPIs) from their game servers running on Google Cloud Platform and monitor the KPIs with low latency. How should they capture the KPIs?  
您的客户希望从其在 Google Cloud Platform 上运行的游戏服务器捕获数 GB 的实时关键绩效指标 (KPI)，并以低延迟监控这些 KPI。他们应该如何捕获这些 KPI？  

A. Store time-series data from the game servers in Google Bigtable, and view it using Google Data Studio.  
B. Output custom metrics to Stackdriver from the game servers, and create a Dashboard in Stackdriver Monitoring Console to view them.  
C. Schedule BigQuery load jobs to ingest analytics files uploaded to Cloud Storage every ten minutes, and visualize the results in Google Data Studio.  
D. Insert the KPIs into Cloud Datastore entities, and run ad hoc analysis and visualizations of them in Cloud Datalab.  

[Discussion](/assets/gcp/discussion/66.md)

# 67

You have a Python web application with many dependencies that requires 0.1 CPU cores and 128 MB of memory to operate in production. You want to monitor and maximize machine utilization. You also want to reliably deploy new versions of the application. Which set of steps should you take?  
您有一个包含许多依赖项的 Python Web 应用程序，在生产环境中运行需要 0.1 个 CPU 核心和 128 MB 内存。您需要监控并最大化机器利用率。您还希望可靠地部署应用程序的新版本。您应该采取哪些步骤？  

A. Perform the following: 1. Create a managed instance group with f1-micro type machines. 2. Use a startup script to clone the repository, check out the production branch, install the dependencies, and start the Python app. 3. Restart the instances to automatically deploy new production releases.  
B. Perform the following: 1. Create a managed instance group with n1-standard-1 type machines. 2. Build a Compute Engine image from the production branch that contains all of the dependencies and automatically starts the Python app. 3. Rebuild the Compute Engine image, and update the instance template to deploy new production releases.  
C. Perform the following: 1. Create a Google Kubernetes Engine (GKE) cluster with n1-standard-1 type machines. 2. Build a Docker image from the production branch with all of the dependencies, and tag it with the version number. 3. Create a Kubernetes Deployment with the imagePullPolicy set to 'IfNotPresent' in the staging namespace, and then promote it to the production namespace after testing.  
D. Perform the following: 1. Create a GKE cluster with n1-standard-4 type machines. 2. Build a Docker image from the master branch with all of the dependencies, and tag it with 'latest'. 3. Create a Kubernetes Deployment in the default namespace with the imagePullPolicy set to 'Always'. Restart the pods to automatically deploy new production releases.  

[Discussion](/assets/gcp/discussion/67.md)

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

# 69

You are running a cluster on Kubernetes Engine (GKE) to serve a web application. Users are reporting that a specific part of the application is not responding anymore. You notice that all pods of your deployment keep restarting after 2 seconds. The application writes logs to standard output. You want to inspect the logs to find the cause of the issue. Which approach can you take?  
您正在 Kubernetes Engine (GKE) 上运行一个集群来服务一个 Web 应用程序。用户报告应用程序的某个特定部分不再响应。您注意到部署中的所有 Pod 都会在 2 秒后重新启动。该应用程序将日志写入标准输出。您想检查日志以找出问题的原因。您可以采取哪种方法？

A. Review the Stackdriver logs for each Compute Engine instance that is serving as a node in the cluster.  
B. Review the Stackdriver logs for the specific GKE container that is serving the unresponsive part of the application.  
C. Connect to the cluster using gcloud credentials and connect to a container in one of the pods to read the logs.  
D. Review the Serial Port logs for each Compute Engine instance that is serving as a node in the cluster.  

[Discussion](/assets/gcp/discussion/69.md)

# 70

You are using a single Cloud SQL instance to serve your application from a specific zone. You want to introduce high availability. What should you do?  
您正在使用单个 Cloud SQL 实例从特定区域为您的应用提供服务。您想要实现高可用性。您应该怎么做？

A. Create a read replica instance in a different region  
B. Create a failover replica instance in a different region  
C. Create a read replica instance in the same region, but in a different zone  
D. Create a failover replica instance in the same region, but in a different zone  

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