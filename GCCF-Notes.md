# Google Cloud Computing Foundations ⚙

$$
\text{Week 0}
$$

→ Router uses Logical addressing system

→ Kernel level threads cannot share the code segment 

→ 192.0.0.0 = Class A (classfull addressing) 

| Protocol  | TCP/IP Layer |
| --- | --- |
| IP ( Internet Protocol) | Network  |
| UDP (User Datagram Protocol) | Transport |
| SMTP (Simple Mail Transfer Protocol) | Application |
| PPP (Point-to-Point Protocol) | Data Link |
- IP
    
    is a protocol, or set of rules, for routing and addressing packets of data so that they can travel across networks and arrive at the correct destination.
    
- PPP
    - used to connect one computer system to another. Computers use PPP to communicate over the telephone network or the Internet. A PPP connection exists when two systems physically connect through a telephone line.
- SMTP
    - It's a set of communication guidelines that allow software to transmit electronic mail over the internet

- UDP
    - allows messaging between different computing devices in a network. *UDP is part of the Internet Protocol (IP) suite of protocols, which defines how data is transmitted over the internet.*
    - uses a connectionless communication model. *It's less reliable than TCP, but it works more quickly.*
    - *Uses - real time multimedia, DNS*

- TCP
    - enables application programs and computing devices to exchange messages over a network.
    - It is designed to send packets across the internet and ensure the successful delivery of data and messages over networks.
    - *Uses - file transfer, email*

### OSI Model

1. Physical Layer: Manages the physical connection and transmission of raw data bits over the network medium.

2. Data Link Layer: Controls data framing, error detection, and access to the physical medium.

3. Network Layer: Routes data packets across networks and provides logical addressing.

4. Transport Layer: Ensures end-to-end communication,routing, error detection, and flow control.

5. Session Layer: Manages session establishment, maintenance, and termination between applications.

6. Session Layer: Manages session establishment, maintenance, and termination between applications.

7. Presentation Layer: Translates, encrypts, and compresses data for application compatibility.

8. Application Layer: Provides user interfaces and network services for applications to interact with the network.

$$
\text{Week 1}
$$

- **IaaS (Infrastructure as a service)**
    
    the service provides the underlying architecture & resources for running servers, but the user is responsible for managing the operating system and application.
    
    → Pay for what you allocate
    

- PaaS **(Platform as a service)**
    
    **t**akes it a step further by managing the entire environment for the user, with only application management required.
    
    → Pay for what you use 
    

- SaaS **(Software as a service)**
    
    goes even further, managing the infrastructure, platform, and software, requiring users to simply bring their data to the system. Examples of SaaS include  SAP and Salesforce.
    

Virtualized data centers offer both IaaS and PaaS options. IaaS provides raw compute, storage, and network resources, while PaaS binds code to libraries that provide access to necessary infrastructure. In the IaaS model, users pay for what they allocate, while in the PaaS model, they pay for what they use. 

### ⭐Services of GCP (Google Cloud Platofrom

1. Compute Engine - IaaS, zonal resource
2. Google Kubernetes Engine - Hybrid 
3. App Engine - PaaS
4. Cloud Functions  - Serverless logic
5. Managed Services - Automated elastic resources 

### What is the Cloud?

The cloud/ cloud computing refers to the software or services that run on the internet (remote servers) rather than locally on a computer

Fundamental Characteristics
→ on-demand self-service, broad network
access, resource pooling, rapid elasticity

### POINTS

→ All GCP resources must be associated with a project 

→ `gsutil` : CL tool used to work with Cloud Storage

→ `gcloud init` : used to setup default config of the Cloud SDK

→ Cloud SDK is a command line used to interface GCP products and services 

→ Cloud Shell is an alternative - provides the same CLI access to cloud rescs from the browser

### QUIZ 1

- Elastic - system can add/remove resources based on need
- Google Cloud Platform Console - web based interface to use GCP
- Storage services for NoSQL DB - Bigtable, Datastore
- You cannot edit GCP project ID after creating the project
- Cloud Datastore is a regional service

$$
\text{Week 2}
$$

### All GCP Services with thier best use case

| GCP Service | Best Use Case |
| --- | --- |
| Compute Engine | Hosting virtual machines for custom workloads. |
| Google Kubernetes Engine | Container orchestration and management. |
| App Engine | Rapid application development and deployment. |
| Cloud Functions | Event-driven serverless computing. |
| Cloud Datastore | NoSQL database for web and mobile applications. |
| Cloud Bigtable | Scalable NoSQL database for large datasets. |
| Cloud Storage | Object storage for unstructured data |
| Cloud Firestore | NoSQL document database for serverless applications |
| BigQuery | High-performance, serverless data analytics. |
| Cloud Machine Learning Engine | Machine learning model training and serving. |
| Cloud Spanner | Globally distributed, strongly consistent database. |
| Cloud Pub/Sub | Real-time messaging and event streaming. |
| Cloud SQL | Managed relational databases. |

### 🔨 Compute Engine (IaaS)

→ infrastructure centric solution 

→ it delivers high performance VMs (Virtual Machines)

→ supports both Windows & Linux

→ You get Custom machine types (up to 160V CPUs, 3.75TB of RAM)

→ Its a Zonal Resource 

→ Network Storage can be attached to VMs as Persistent Disks (PDs)

- *PDs are a cost effective, go to option for non-volatile data*

### 🔨 App Engine (PaaS)

→ Lets users focus on the code rather than the infrastructure 

→ its a fully managed environment 

→ eliminates any need for hardware/infra 

→ can use a range of languages (C, python, java, php, .NET, node JS, Go, Ruby)

→ enables users to build their applications as decoupled micro services.

→ it has *Automatic Scaling, Load balancing* 

### 🔨 Google Kubernetes Engine (Hybrid)

→ GKE is a managed environment for deploying containerized apps

→  Its a hybrid between IaaS (CE) & PaaS (AE)

→ Ideal for users who are managing a fleet of VMs, this provides a easier way (i.e. Containerization)

→ Easier & cost effective to scale an application 

→ “IaaS flexibility with PaaS scalability”

→ Containers provide an abstraction layer of the hardware & OS

---

- KUBERNETES
    
    open source container orchestration tool for automating the management/deployment of containerized apps
    
- DOCKER
    
    platform fro developing & shipping apps in containers
    
    Containers - lightweight portable enviornments that include everything required to run an application
    
    ---
    

### 🔨 Cloud Functions (Serverless)

→ Cloud functions are used to build and deploy services at the level of individual functions.

→ Eliminate the need for server and infrastructure management.

→ They can scale very easily with little additional work

→ Cloud functions are like building blocks, adjustable and integratable with third-party services and APIs.

- They connect and extend cloud services by responding to *Cloud Events.*
    
     Cloud events are actions in the cloud environment, triggering functions when, for instance, data changes or files are added.
    

### QUIZ 2 - IMP POINTS

- Hypervisor -A software program that creates and manages VMs
- IOPS is a measure of the performance of a Solid-State Drive (SSD) persistent disk, 
A higher IOPS rating indicates that the disk can perform more operations per second.

$$
\text{Week 3}
$$

**Cloud SQL:**

- Managed Relational database service.
- Supports MySQL, PostgreSQL, and SQL Server.
- Ideal for web applications, e-commerce, and mobile apps.

**Cloud Bigtable:**

- NoSQL, massively scalable database.
- uses Colossus file system
- Used for real-time analytics and MapReduce operations
- Designed for large analytical and operational workloads.

**Cloud Spanner:**

- Globally distributed, horizontally scalable database.
- Minimum 3 nodes are required in cloud spanner instance
- Combines the benefits of NoSQL and SQL databases.
- Suitable for mission-critical, globally scaled applications

**BigQuery:**

- Fully managed, serverless data warehouse.
- Analyze large datasets with SQL-like queries.
- Ideal for business intelligence and data analytics.

**Cloud Storage:**

- Object storage service for storing and retrieving data.
- Scalable, durable, and cost-effective.
- Used for backups, content delivery, and maintaining data

**Cloud Datastore:**

- NoSQL database for web and mobile applications.
- Serverless and schemaless
- Scalable and fully managed.
- Suitable for user profiles, metadata, and application state.
