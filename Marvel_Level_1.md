```
TASK 1: Working of a Version Control
````


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

```
TASK 8: IaaS, PaaS and SaaS
```


## **Cloud and Cloud Providers**

## **1. What is Cloud?**

The **cloud** is a network of remote servers that store, manage, and process data over the internet instead of local computers.
It provides **on-demand access** to computing resources without owning hardware.

**Key Points:**

* Accessible via the internet
* Scalable and flexible
* Offers storage, compute, and software services
* Examples: Google Drive, AWS, Azure

---

## **2. What is a Cloud Provider?**

A **cloud provider** offers computing resources and services over the internet.
They manage physical infrastructure while users access virtual resources.

**Examples:** AWS, Microsoft Azure, Google Cloud, IBM Cloud, Oracle Cloud

---

## **3. Types of Cloud Service Models**

### **a) Infrastructure as a Service (IaaS)**

Provides **virtualized IT infrastructure**—compute, storage, and networking—on a **pay-as-you-go** basis.

**Key Points:**

* Users rent virtual machines and configure OS/software
* Based on **virtualization**
* Customizable (CPU, RAM, storage, networking)

**Examples:**
AWS EC2, Azure Virtual Machines, Google Compute Engine

**Benefits:**

* Cost-effective
* Scalable and flexible
* Reliable and secure

**Use Case:**
A startup hosts its e-commerce site using AWS EC2, S3, and VPC for secure, scalable infrastructure.

---

### **b) Platform as a Service (PaaS)**

Provides a **complete environment** for developing, running, and managing applications — without managing servers.

**Key Points:**

* Developers focus on code, not infrastructure
* Platform includes OS, frameworks, and tools
* Based on **abstraction**

**Examples:**
Google App Engine, AWS Elastic Beanstalk, Azure App Service

**Benefits:**

* Faster development
* Automatic scaling
* Simplified deployment and maintenance

**Use Case:**
A developer uploads code to AWS Elastic Beanstalk; the platform auto-deploys and scales the app.

---

### **c) Software as a Service (SaaS)**

Delivers **ready-to-use software** over the internet. Users access apps via a browser — no installation needed.

**Key Points:**

* Based on **multi-tenancy** (shared but secure architecture)
* Provider manages hosting, updates, and security
* Subscription-based access

**Examples:**
Google Workspace, Microsoft 365, Salesforce, Zoom, Dropbox

**Benefits:**

* Accessible anywhere
* Automatic updates
* Cost-efficient and scalable

**Use Case:**
A business uses Google Workspace for emails, file sharing, and collaboration — no server setup needed.

---


