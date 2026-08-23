
# Cloud Provider Comparison

This document compares the core infrastructure services offered by the three leading public cloud providers — Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP) — based on their official documentation.

## Comparison Table

| Infrastructure Component | AWS | Microsoft Azure | Google Cloud Platform |
|---|---|---|---|
| Compute | EC2 (Elastic Compute Cloud) | Virtual Machines | Compute Engine |
| Storage | S3 (Simple Storage Service), EBS (Elastic Block Store) | Blob Storage, Managed Disks | Cloud Storage, Persistent Disk |
| Networking | VPC (Virtual Private Cloud) | Virtual Network (VNet) | VPC (Virtual Private Cloud) |
| Identity and Access Management (IAM) | AWS IAM | Microsoft Entra ID (formerly Azure AD) | Cloud IAM |

## Guide Questions

**1. Which cloud provider offers the broadest range of services? Explain your answer.**

AWS is generally recognized as offering the broadest range of services, with hundreds of products spanning compute, storage, databases, machine learning, IoT, and more. This is largely due to AWS being the first major public cloud provider (launched in 2006), giving it the longest head start to build out a mature and extensive service catalog.

**2. Which cloud platform would you recommend for an organization that primarily uses Microsoft products?**

Microsoft Azure would be the best fit for an organization already invested in Microsoft products (Windows Server, Active Directory, Office 365, .NET). Azure offers native, tightly integrated support for these tools, which reduces licensing complexity and simplifies identity management through Microsoft Entra ID.

**3. Which platform is widely recognized for Artificial Intelligence (AI), Machine Learning (ML), and Kubernetes services?**

Google Cloud Platform is widely recognized in this space. Google originally developed Kubernetes and offers Google Kubernetes Engine (GKE) as a mature, heavily-used managed service, while its Vertex AI platform and TensorFlow integration make it a strong choice for AI/ML workloads.

**4. What similarities did you observe among the three cloud providers?**

All three providers offer conceptually equivalent services under different names — virtual machines for compute, object/block storage for data persistence, virtual networks for connectivity, and IAM systems for access control. Each also follows a pay-as-you-go pricing model, provides global data center regions, and emphasizes scalability, security, and infrastructure-as-code tooling (CloudFormation, ARM/Bicep templates, and Deployment Manager, respectively).
