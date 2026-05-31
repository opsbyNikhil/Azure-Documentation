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
- [How to create VM in Azure](#how-to-create-vm-in-azure)
  - [🚀 1. Images](#-1-images)
    - [a. Marketplace Image](#a-marketplace-image)
    - [b. Custom Images](#b-custom-images)
    - [c. Shared Images (Community Images)](#c-shared-images-community-images)
    - [d. Managed Images](#d-managed-images)
  - [💾 2. Disk Types](#-2-disk-types)
    - [a. OS Disk](#a-os-disk)
    - [b. Data Disk](#b-data-disk)
    - [c. Temporary Disk / Local Storage](#c-temporary-disk--local-storage)
  - [🌐 3. Networking](#-3-networking)
    - [VM Networking Flow:](#vm-networking-flow)
  - [🔐 4. Authentication](#-4-authentication)
    - [Options:](#options)
    - [Best Practice:](#best-practice)
  - [⚙️ 5. VM Sizes](#️-5-vm-sizes)
  - [🏗️ 6. VM Architecture Overview](#️-6-vm-architecture-overview)

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

![OveralAzure](./Images/Azure-1.png)

---

# How to create VM in Azure

## 🚀 1. Images

Azure VM creation starts with selecting an image:

### a. Marketplace Image
- Pre-built images provided by Azure
- Examples:
  - Ubuntu
  - Red Hat
  - Windows Server

---

### b. Custom Images
- Your own VM image created from an existing machine
- Used for:
  - Project-specific environments
  - Pre-configured applications
  - Reusable VM templates

---

### c. Shared Images (Community Images)
- Images shared across regions or organizations
- Example:
  - Image created in `central india` can be used in `ap-south-2`
- Useful for:
  - Cross-region deployments
  - Standardized environments

---

### d. Managed Images
- Lightweight reusable VM images
- Used for quick deployments
- Example:
  - Nginx server image
- Best for:
  - Small, repeated deployments
  - Fast provisioning

---

## 💾 2. Disk Types

### a. OS Disk
- Stores operating system files
- Fully persistent storage
- Type: **Non-ephemeral**
- Data is NOT lost if VM stops or restarts

---

### b. Data Disk
- Used for application data
- Attached separately from OS disk
- Can be expanded independently

---

### c. Temporary Disk / Local Storage
- Used for cache and temporary files
- Type: **Ephemeral storage**
- Data is LOST when VM is deleted or restarted
- Best for:
  - Temporary processing
  - Cache files

---

## 🌐 3. Networking

VM networking components:

- **Virtual Network (VNet / VPC equivalent)**
- **Network Interface (NIC)**
- **Public IP Address**
- **Network Security Group (NSG)**

### VM Networking Flow:


- > VM → Network Interface → VNet → Public IP → NSG Rules


---

## 🔐 4. Authentication

### Options:

- Username & Password
- SSH Key-Based Authentication (Recommended)

### Best Practice:
- Use SSH keys for Linux VMs
- More secure than password-based login

---

## ⚙️ 5. VM Sizes

- Defines CPU, Memory, and performance capacity
- Choose based on workload:
  - Web apps → General Purpose
  - Heavy compute → Compute Optimized
  - Large memory apps → Memory Optimized
  - Big data → Storage Optimized
  - AI/ML → GPU Optimized

---

## 🏗️ 6. VM Architecture Overview

![VM Architecture Overview](./Images/Azure-2.png)

---
