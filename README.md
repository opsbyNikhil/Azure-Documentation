# 📘 Cloud Computing & Azure VM Notes

## 📑 Index

- [📘 Cloud Computing \& Azure VM Notes](#-cloud-computing--azure-vm-notes)
  - [📑 Index](#-index)
  - [☁️ Cloud Deployment Models](#️-cloud-deployment-models)
    - [1. On-Premises](#1-on-premises)
    - [2. Infrastructure as a Service (IaaS)](#2-infrastructure-as-a-service-iaas)
    - [3. Platform as a Service (PaaS)](#3-platform-as-a-service-paas)
    - [4. Software as a Service (SaaS)](#4-software-as-a-service-saas)
    - [5. Function as a Service (FaaS)](#5-function-as-a-service-faas)
  - [☁️ Ways to Create a VM in Azure](#️-ways-to-create-a-vm-in-azure)
  - [💻 Types of Azure Virtual Machines](#-types-of-azure-virtual-machines)
    - [1. General Purpose](#1-general-purpose)
    - [2. Compute Optimized](#2-compute-optimized)
    - [3. Memory Optimized](#3-memory-optimized)
    - [4. Storage Optimized](#4-storage-optimized)
    - [5. GPU Accelerated](#5-gpu-accelerated)
  - [🧩 Azure VM Naming Convention](#-azure-vm-naming-convention)
    - [Example: `DCads_v5`](#example-dcads_v5)
    - [Example: `DC8ads_v5`](#example-dc8ads_v5)
- [Azure Info](#azure-info)

---

## ☁️ Cloud Deployment Models

### 1. On-Premises
- No cloud involvement
- Everything is managed by the DevOps engineer
- Full responsibility includes:
  - Infrastructure
  - Servers
  - Networking
  - Storage
  - OS
  - Runtime
  - Middleware
  - Applications
  - Data

---

### 2. Infrastructure as a Service (IaaS)
**Cloud provides:**
- Virtualization
- Servers
- Storage
- Networking

**Customer responsibility:**
- Operating System (OS)
- Middleware
- Runtime
- Applications
- Data

---

### 3. Platform as a Service (PaaS)
**Cloud provides:**
- Virtualization
- Servers
- Storage
- Networking
- Operating System (OS)
- Middleware
- Runtime

**Customer responsibility:**
- Applications
- Data

**Examples:**
- Azure App Service  
- AWS Elastic Beanstalk  

---

### 4. Software as a Service (SaaS)
**Cloud provides everything:**
- Application
- Data
- Runtime
- Middleware
- OS
- Storage
- Servers
- Networking
- Virtualization

**User responsibility:**
- Only usage of the application

---

### 5. Function as a Service (FaaS)
- Serverless computing model
- No server management required
- You only deploy code functions
- Automatically scaled and executed

**Example:**
- Azure Functions  

---

## ☁️ Ways to Create a VM in Azure

1. **Azure Portal (GUI)**
2. **Azure CLI (Command Line Interface)**
3. **Infrastructure as Code (IaC)**
   - Terraform
   - ARM Templates
   - Azure Bicep

---

## 💻 Types of Azure Virtual Machines

### 1. General Purpose
- Balanced CPU-to-memory ratio
- Suitable for web apps and small databases

---

### 2. Compute Optimized
- High CPU-to-memory ratio
- Suitable for high-performance computing

---

### 3. Memory Optimized
- High memory-to-CPU ratio
- Suitable for in-memory databases and analytics

---

### 4. Storage Optimized
- High disk throughput and IOPS
- Suitable for Big Data, SQL, NoSQL, Data Warehousing

---

### 5. GPU Accelerated
- GPU powered machines
- Suitable for AI/ML, graphics rendering, video processing

---

## 🧩 Azure VM Naming Convention

### Example: `DCads_v5`

- **D** → VM Family  
- **C** → Sub-family  
- **a** → Feature 1  
- **d** → Feature 2  
- **s** → Feature 3  
- **v5** → Version  

---

### Example: `DC8ads_v5`

- **D** → VM Family  
- **C** → Sub-family  
- **8** → vCPU count  
- **a** → Feature 1  
- **d** → Feature 2  
- **s** → Feature 3  
- **v5** → Version  

---

# Azure Info

#[OveralAzure](./Images/Azure-1.png)