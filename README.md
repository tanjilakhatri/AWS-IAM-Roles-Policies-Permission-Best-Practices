# 🔐 AWS IAM Security Project

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?logo=amazonaws)
![IAM](https://img.shields.io/badge/Service-IAM-blue)
![EC2](https://img.shields.io/badge/EC2-Amazon-yellow)
![S3](https://img.shields.io/badge/S3-Storage-green)
![Status](https://img.shields.io/badge/Project-In%20Progress-success)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

A hands-on AWS cloud security project that demonstrates how to implement Identity and Access Management (IAM) using industry best practices.

This project focuses on creating IAM users, groups, custom policies, IAM roles, Multi-Factor Authentication (MFA), and permission validation to secure AWS resources based on user responsibilities.

---

## 📌 Project Overview

## 📑 Table of Contents

- [Project Overview](#-project-overview)
- [Objectives](#-objectives)
- [AWS Services Used](#-aws-services-used)
- [Project Architecture](#-project-architecture)
- [Project Implementation](#-project-implementation)
- [Project Folder Structure](#-project-folder-structure)
- [Project Screenshots](#-project-screenshots)
- [Security Best Practices](#-security-best-practices)
- [Learning Outcomes](#-learning-outcomes)
- [Future Improvements](#-future-improvements)
- [Author](#-author)

In a real organization, different teams require different levels of access to AWS services. Providing the same permissions to every user can create security risks.

This project simulates a company environment where Developers, DevOps Engineers, and Auditors require different permissions based on their job roles. Using AWS IAM, secure access control is implemented by creating users, groups, policies, and roles while following the Principle of Least Privilege.

---

## 🎯 Objectives

- Create IAM users for different departments.
- Organize users into IAM groups.
- Create and attach custom IAM policies.
- Configure secure access to an Amazon S3 bucket.
- Create an IAM role for an EC2 instance.
- Enable Multi-Factor Authentication (MFA).
- Validate user permissions.
- Implement AWS IAM security best practices.

---

## 🛠 AWS Services Used

- AWS Identity and Access Management (IAM)
- Amazon Simple Storage Service (S3)
- Amazon Elastic Compute Cloud (EC2)
- AWS CloudWatch
- Multi-Factor Authentication (MFA)

---

## 🏗 Project Architecture

> Architecture diagram will be added after completing the implementation.

```
                 AWS Account
                      │
      ┌───────────────┼───────────────┐
      │               │               │
 Developers        DevOps         Auditors
      │               │               │
 Custom Policy   Custom Policy   ReadOnlyAccess
      │
 Amazon S3 Bucket
      │
 EC2 Instance
      │
 IAM Role
```

---

## 🚀 Project Implementation

The following steps were performed to implement secure Identity and Access Management (IAM) in AWS.

### Step 1: Created IAM Users

Created six IAM users to represent different departments within the organization.

**Users Created:**
- developer1
- developer2
- devops1
- devops2
- auditor1
- auditor2

📷 **Screenshot**

<p align="center">
  <img src="screenshots/iam-users.png" width="900">
</p>

---

### Step 2: Created IAM Groups

Three IAM groups were created to manage permissions efficiently.

**Groups Created:**
- Developers
- DevOps
- Auditors

Each user was added to the appropriate group based on their job role.

📷 **Screenshot**

<p align="center">
  <img src="screenshots/iam-groups.png" width="900">
</p>

---

### Step 3: Created Amazon S3 Bucket

An Amazon S3 bucket was created to store project files and test user permissions.

**Bucket Name**

```
company-project-storage
```

Sample files were uploaded to verify access permissions.

📷 **Screenshot**

<p align="center">
  <img src="screenshots/s3-bucket.png" width="900">
</p>

---

### Step 4: Created IAM Policies

Custom IAM policies were created based on the responsibilities of each team.

#### Developers Policy

Allowed permissions:
- List Bucket
- Upload Objects
- Download Objects

#### DevOps Policy

Allowed permissions:
- EC2 Management
- CloudWatch Access
- IAM Read Permissions

#### Auditors

Attached AWS Managed Policy:

- ReadOnlyAccess

📷 **Screenshot**

<p align="center">
  <img src="screenshots/iam-policies.png" width="900">
</p>

---

### Step 5: Created IAM Role

Created an IAM role named:

```
EC2-S3-Access-Role
```

Attached:

```
AmazonS3ReadOnlyAccess
```

The role was assigned to an EC2 instance to provide secure access to the S3 bucket without storing access keys.

📷 **Screenshot**

<p align="center">
  <img src="screenshots/iam-role.png" width="900">
</p>

---

## 📁 Project Folder Structure

```
aws-iam-security-project
│
├── architecture/
│   └── architecture.png
│
├── policies/
│   ├── developers-policy.json
│   └── devops-policy.json
│
├── screenshots/
│   ├── iam-users.png
│   ├── iam-groups.png
│   ├── s3-bucket.png
│   ├── iam-policies.png
│   ├── iam-role.png
│   └── permission-test.png
│
├── README.md
├── LICENSE
└── .gitignore
```
