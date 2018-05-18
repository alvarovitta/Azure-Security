# Securing PaaS Resources
In Platform as a service (PaaS) scenarios, web apps, storage and databases are the main workloads for organizations that use cloud computing. By nature Paas services have public endpoint, we need to be careful on their security. 
 
- Azure App Service is a PaaS offering that lets you create web and mobile apps for any platform or device and connect to data anywhere, in the cloud or on-premises.  


- Azure SQL Database and SQL Data Warehouse provide a relational database service for your Internet-based applications.  


- Azure makes it possible to deploy and use storage in ways not easily achievable on-premises. With Azure storage, you can reach high levels of scalability and availability with relatively little effort.  



 


## Guidance for App Service 

- Authenticate through Azure Active Directory (AD), App Service provides an OAuth 2.0 service for your identity provider.  

- Restrict access based on the need to know and least privilege security principles. Role-Based Access Control (RBAC) can be used to assign permissions to users, groups, and applications at a certain scope. 

- Use Azure Key Vault to safeguard cryptographic keys and secrets used by cloud applications and services. .  

- Use App Service Environment's  virtual network integration feature to restrict incoming source IP addresses through network security groups (NSGs) and run Web App in isolated environment. 


## Guidance for PaaS Databases 

- Use a centralized identity repository for authentication and authorization 


- Restrict Access based on IP Address 


- Encryption of data at rest 



## Guidance for Azure Storage 

- Use Shared Access Signature instead of a storage account key as it allows you to share content the way you want to share it without giving away your Storage Account Keys.  

- Use managed disks for VMs and let Azure manage the storage accounts that you use for VM disks. 


- Use Role-Based Access Control, With RBAC, you focus on giving employees the exact permissions they need, based on the need to know and least privilege security principles. 


- Use client-side encryption for high value data, it enables you to programmatically encrypt data in transit before uploading to Azure Storage and programmatically decrypt data when retrieving it from storage. 


- Use Azure Disk Encryption for VMs, it helps you encrypt your Windows and Linux IaaS virtual machine disks.  


- Enable Storage Service Encryption to automatically encrypt data. 



## Next steps 
Securing your Network 
