
 # **TASK 1: Working of a Version Control**



---

## **Version Control Systems (VCS)**

Version Control Systems (VCS) are tools that help developers manage changes to source code over time.
They allow multiple people to work on a project simultaneously, track every modification, and revert to previous versions if necessary.



---

## **2. Core Concepts**

### **a. Repository**

A **repository (repo)** is the central location where all project files and their revision history are stored.

* **Local repository:** Exists on your computer.
* **Remote repository:** Hosted online (e.g., GitHub, GitLab, Bitbucket).

---

### **b. Commit**

A **commit** records changes made to files in the repository.

Each commit includes:

* A unique **ID (hash)**
* **Author details**
* **Commit message** describing the change

---

### **c. Branch**

A **branch** is an independent line of development.

* The default branch is usually called **main** or **master**.
* Developers create new branches to work on features without affecting the main codebase.

---

### **d. Merge**

**Merging** combines the changes from one branch into another.
For example, merging a `feature` branch into `main` after development is complete.

---

### **e. Revert**

`git revert` undoes the effects of a specific commit by creating a new commit that reverses its changes.

---

### **f. Cherry-pick**

`git cherry-pick` allows you to apply a specific commit from one branch onto another without merging the entire branch.

---
# **TASK 2: Database task - DynamoDB**


In this task, I learned how to use Amazon DynamoDB, a fully managed NoSQL database provided by Amazon Web Services. I created a simple user login system where user credentials were stored securely in a DynamoDB table using a partition key. I implemented user registration (write operation using WCU) and login validation (read operation using RCU). I understood how DynamoDB handles scaling, replication across Availability Zones, and throttling when capacity limits are exceeded. I also learned the difference between NoSQL databases like DynamoDB and relational databases like MySQL, especially in terms of schema design, scalability, and performance.

| Server       |     command |
|--------------|--------------|
| ![Img1](https://raw.githubusercontent.com/Anjan28052006/Marvel_Level_1.0/refs/heads/main/Screenshot%202026-02-27%20050208.png)| ![Img2](https://raw.githubusercontent.com/Anjan28052006/Marvel_Level_1.0/refs/heads/main/Screenshot%202026-02-27%20050650.png) |

---

# **TASK 3: Create an application on EC2 instance**
### EC2 (IaaS) Short Report

The objective of this task was to understand the working of **Amazon EC2**, an **Infrastructure as a Service (IaaS)** that allows users to choose and manage the operating system, storage, security, and monitoring. An EC2 instance was launched using **Amazon Linux 2023 (Kernel 6.1)** with **1×8 GiB gp3 EBS storage**, which provides general-purpose performance with **3000 IOPS**.

Security was implemented using **security groups** to allow SSH access only from a specific IP and **SSH key-based authentication** using the **RSA algorithm**. The instance was accessed using the SSH command:

```bash
ssh -i key.pem ec2-user@<Public-IP>
```

This task provided hands-on experience in configuring EC2 resources and demonstrated how dynamic applications can be deployed using AWS EC2.


![Img1](https://raw.githubusercontent.com/Anjan28052006/Marvel_Level_1.0/refs/heads/main/Screenshot%202026-01-12%20214948.png)
---

# **TASK 4: AWS CloudFront – Serving Content from Multiple S3 Buckets**

The objective of this task was to understand the use of **Amazon CloudFront** as a Content Delivery Network (CDN) and its integration with **Amazon S3**. CloudFront delivers content with low latency by caching data at globally distributed edge locations, while S3 acts as the origin for storing static content.

In this task, **multiple S3 buckets** were created to store different types of content such as website files and images. These buckets were configured as **origins** in a CloudFront distribution, and **path-based routing** was used to route requests to the appropriate S3 bucket.

When a user accesses the CloudFront URL, the request is routed to the nearest edge location. If the content is cached, it is served immediately; otherwise, CloudFront fetches the content from the respective S3 bucket, delivers it to the user, and caches it for future requests.

This implementation improves performance, reduces latency, minimizes load on S3, and enables scalable global content delivery.

[CloudFront Distribution URL](https://dslvx59l94fp9.cloudfront.net/TvShows.html)

---

# **TASK 5: Introduction to Kali Linux & Basic Penetration Testing**

In this task, I learned about Kali Linux, a Linux distribution specifically designed for penetration testing and security auditing. Kali Linux contains many pre-installed tools used to identify vulnerabilities, scan networks, and test system security.

We performed a basic penetration test on an intentionally vulnerable virtual machine called `Metasploitable 2`. The attacker machine (`Kali Linux`) and the target machine (`Metasploitable 2`) were configured on the same network to ensure proper communication between them.

We used `Nmap (Network Mapper)` to scan the target system using the command:
```
nmap -sV <IP_address>
```

The -sV option was used to detect service versions running on open ports. From the scan results, we identified multiple open ports, including FTP running on Port 21. The scan revealed that the FTP service was running `vsftpd 2.3.4`, a version known to contain a **backdoor vulnerability**.

To exploit this vulnerability, we used the Metasploit Framework. We launched Metasploit using `msfconsole` and selected the appropriate exploit module:
```
use exploit/unix/ftp/vsftpd_234_backdoor
```

After configuring the target IP address , we executed the exploit. Upon successful exploitation, a remote command shell was obtained, demonstrating how attackers can gain unauthorized access if services are outdated and unpatched.

![img](https://raw.githubusercontent.com/Anjan28052006/Marvel_Level_1.0/refs/heads/main/WhatsApp%20Image%202026-02-26%20at%207.36.06%20PM.jpeg)

---

# **TASK 6: Socket.IO**

## **Socket.IO - Real-Time Communication**

Socket.IO enables **real-time, bi-directional communication** between clients and server.  
- **io**: Server, manages all clients, broadcasts, handles rooms.  
- **socket**: Single client connection, sends/receives messages, joins rooms.  

**Messaging:** `io.emit()` → all, `socket.broadcast.emit()` → all except sender, `io.to(socketID).emit()` → private.  
**Rooms:** `socket.join('room')`, `io.to('room').emit()`.  
**Private chat:** Messages go **through server**.  
**Online users:** Track on server, broadcast updates.


| tab1      |     tab2 |
|--------------|--------------|
| ![Img1](https://raw.githubusercontent.com/Anjan28052006/Marvel_Level_1.0/refs/heads/main/Screenshot%202026-01-11%20105330.png)| ![Img2](https://raw.githubusercontent.com/Anjan28052006/Marvel_Level_1.0/refs/heads/main/Screenshot%202026-01-11%20105351.png) |



# **TASK 7: OSI Model**

The objective of this task was to understand the **OSI (Open Systems Interconnection) model**, its seven-layer architecture, and its importance in computer networking and cloud computing. The OSI model provides a standard framework that explains how data is transmitted across a network from one system to another.

A simple visual representation of the OSI model was created using a cloud-based diagramming tool such as **Draw.io** to clearly illustrate the flow of data through each layer.

![img](https://raw.githubusercontent.com/Anjan28052006/Marvel_Level_1.0/refs/heads/main/OSI.drawio.png)

[Breif Explaination](https://anjan28052006.github.io/OSI/)  
[YouTube Resources](https://www.youtube.com/watch?v=vv4y_uOneC0)

# **TASK 8: IaaS, PaaS and SaaS**



## Cloud Service Models: IaaS, PaaS, SaaS

Cloud computing provides different levels of services depending on how much control and responsibility the user wants.

 **IaaS (Infrastructure as a Service)** delivers virtualized computing resources such as servers, storage, and networking over the internet. Users manage the operating system, applications, and data, while the provider handles physical hardware and networking. It is flexible, scalable, and ideal for custom setups. Examples include AWS EC2, Azure Virtual Machines, and Google Compute Engine.

**PaaS (Platform as a Service)** offers a complete platform for developing, testing, and deploying applications without managing the underlying infrastructure. Users focus on their applications and data, while the provider manages runtime, servers, networking, and storage. This allows faster development, automatic scaling, and simplified deployment. Examples include AWS Elastic Beanstalk, Google App Engine, and Azure App Service.

**SaaS (Software as a Service)** delivers ready-to-use software accessible through a browser. Users do not manage infrastructure or platforms; the provider handles everything including hosting, updates, and security. SaaS offers quick access, anywhere usage, and low maintenance. Examples include Google Workspace, Microsoft 365, Zoom, and Salesforce.

Together, these service models provide a spectrum of cloud services from full control (IaaS) to fully managed applications (SaaS), allowing businesses and developers to choose the level of management that fits their needs.

---
**#TASK 9: Encryption Techniques - Secure Messaging App**

---
Encryption is the process of converting plaintext into ciphertext to ensure secure communication. In this task, classical ciphers such as `Caesar`, `Vigenère`, and `substitution cipher` were studied along with modern encryption techniques. `Symmetric encryption` uses a single secret key for both encryption and decryption, while `asymmetric encryption` uses public and private keys, such as in `RSA`, which relies on large prime numbers for security. Encryption differs from hashing algorithms like `SHA-256`, as encryption is reversible whereas hashing is not. A simple secure chat application was implemented using Python and PyCrypto to encrypt and decrypt messages successfully.

`Example for word HELLO`
```python
HELLO
  ↓
HELLO + spaces (to make 16 bytes)(padding)
  ↓
Converted to bytes
  ↓
Encrypted using AES key
  ↓
Converted to Base64
  ↓
Sent
  ↓
Base64 decoded
  ↓
Decrypted using same key
  ↓
Spaces removed
  ↓
HELLO

```
![img](https://raw.githubusercontent.com/Anjan28052006/Marvel_Level_1.0/refs/heads/main/Screenshot%202026-02-27%20070113.png)

---

# **TASK 10: IP Addressing and Web Scraping - Job Listings Scraper**

## Job Listings Scraper

Used Python, Selenium, and BeautifulSoup to scrape software engineer jobs from Indeed India.  
Selenium opens a real browser to load dynamic content, while BeautifulSoup parses the HTML.  
Extracted job titles, company, and location.  
Selenium is needed because requests + BeautifulSoup alone cannot access JavaScript-loaded jobs.  
Successfully retrieved multiple job postings in real-time.

![img](https://raw.githubusercontent.com/Anjan28052006/Marvel_Level_1.0/refs/heads/main/Screenshot%202026-01-13%20081121.png)


