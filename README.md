# 🔐 AWS IAM Security Project

A hands-on AWS cloud security project that demonstrates how to implement Identity and Access Management (IAM) using industry best practices.

This project focuses on creating IAM users, groups, custom policies, IAM roles, Multi-Factor Authentication (MFA), and permission validation to secure AWS resources based on user responsibilities.

---

## 📌 Project Overview

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
