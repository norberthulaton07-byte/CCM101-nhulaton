# Cloud Provider Comparison

## Infrastructure Component Comparison

| Infrastructure Component | AWS | Microsoft Azure | Google Cloud Platform |
|---------------------------|-----|------------------|------------------------|
| Compute | Amazon EC2 lets users launch and manage virtual servers, choosing from a wide range of instance types based on CPU, memory, and workload needs. | Azure Virtual Machines lets users deploy Windows or Linux based servers in the cloud, with flexible sizing options to match performance requirements. | Google Compute Engine lets users create virtual machines using either predefined machine types or custom configurations tailored to specific workloads. |
| Storage | Amazon S3 is an object storage service used to store and retrieve any amount of data, commonly used for backups, media files, and static websites. | Azure Blob Storage is Microsoft's object storage solution, designed to hold large amounts of unstructured data such as documents, images, and backups. | Google Cloud Storage offers object storage for unstructured data, with different storage classes available depending on how frequently the data needs to be accessed. |
| Networking | Amazon VPC allows users to create an isolated virtual network within AWS, giving full control over IP ranges, subnets, and routing. | Azure Virtual Network (VNet) allows resources to communicate securely with each other, the internet, and on-premises networks. | Google VPC provides a global virtual network that can span multiple regions while still supporting custom subnets and firewall rules. |
| Identity and Access Management (IAM) | AWS IAM controls who can access AWS resources and what actions they're allowed to perform, using users, groups, roles, and policies. | Azure Active Directory (Azure AD) manages user identities and controls access to Azure resources and Microsoft services. | Google Cloud IAM lets administrators define fine-grained permissions, controlling which users or service accounts can access specific GCP resources. |

## Guide Questions

**1. Which cloud provider offers the broadest range of services? Explain your answer.**

AWS offers the broadest range of services among the three providers. It launched earliest, in 2006, and has since built out one of the largest and most mature service catalogs in the industry, covering everything from basic compute and storage to specialized tools for AI, IoT, and analytics.

**2. Which cloud platform would you recommend for an organization that primarily uses Microsoft products? Why?**

Microsoft Azure would be the strongest choice for an organization already built around Microsoft tools. Because Azure was designed to work closely with products like Windows Server, Active Directory, and Microsoft 365, it typically requires less setup and integration work for teams already inside that ecosystem.

**3. Which platform is widely recognized for Artificial Intelligence (AI), Machine Learning (ML), and Kubernetes services?**

Google Cloud Platform is the provider most closely associated with AI, ML, and Kubernetes. Kubernetes itself originated from an internal Google project before becoming open source, and GCP continues to be known for strong machine learning and large-scale data analytics tools.

**4. What similarities did you observe among the three cloud providers?**

Despite using different product names, all three providers offer the same core categories of infrastructure: virtual compute instances, object storage, isolated virtual networks, and identity/access management systems. All three also follow a pay-as-you-go pricing model and allow resources to be scaled on demand rather than requiring upfront hardware investment.
