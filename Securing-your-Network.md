
As organizations move their workloads to public clouds, it is critical to support similar capabilities for perimeter network architecture in Azure to meet compliance and security requirements. 


Use the following questions to assist in designing your network security strategy: 
 
- How can a perimeter network in Azure be built? 

- What are some of the Azure features available to build the perimeter network? 

- How can back-end workloads be protected? 

- How are Internet communications controlled to the workloads in Azure? 

- How can the on-premises networks be protected from deployments in Azure? 

- When should native Azure security features be used versus third-party appliances or services? 

The following diagram shows various layers of security Azure provides to customers. These layers are both native to the Azure platform itself and customer-defined features: 



Machine generated alternative text: Azure Deployments Network Virtual NSG& Virtual Network Public IP Isolation Appliances UDR Azure DDoS Intemet 



## Guidance 


The following lists the best practices when designing your Azure network security: 


- Logically segment subnets:  Create a single, private IP address space-based network for your Azure Virtual Machines. Segment the larger address space into subnets.  


- Control routing behavior:  Customize the routing configuration for VMs in your deployments. Configure user-defined routes when deploying a VN security appliance. 

- Enable Forced Tunneling:  Enable forced tunneling on your VMs when you have cross-premises connectivity between your Azure Virtual Network and your on-premises network.  

- Use virtual network appliances:   Enable security at high levels of the stack, deploy virtual network security appliances provided by Azure partners. 

- Deploy DMZs for security zoning: DMZs focus network access control management, monitoring, logging, and reporting on the devices at the edge of the Azure Virtual Network.  

- Avoid exposure to the Internet with dedicated WAN links:  For exceptional levels of security or performance for your cross-premises connections, use Azure ExpressRoute for your cross-premises connectivity.   

- Optimize uptime and performance:  Confidentiality, integrity, and availability (CIA) is a widely accepted security model. To optimize service availability and performance, use load balancing. 

- HTTP-based Load Balancing:  Use the Azure Application Gateway as the HTTP load balancer for deployments such as: 

  - Applications that require requests from the same user/client session to reach the same back-end virtual machine. Examples of this would be shopping cart apps and web mail servers. 


  - Applications that want to free web server farms from SSL termination overhead by taking advantage of Application Gateway’s SSL offload feature. 


  - Applications, such as a content delivery network, that requires multiple HTTP requests on the same long-running TCP connection to be routed or load balanced to different back-end servers. 


- External Load Balancing:  External load balancing takes place when incoming connections from the Internet are load balanced among your servers located in an Azure Virtual Network.  


- Internal Load Balancing:  Internal load balancing is similar to external load balancing. Internal load balancer accepts connections from VMs that are not on the Internet.   

- Use Global Load Balancing:  Public cloud computing deploys globally distributed applications that have components located in data centers around the world. Use global load balancing to make services available even when entire data centers become unavailable. 

- Disable RDP/SSH Access to Azure Virtual Machines:  It is possible to reach Azure VMs using RDP and SSH protocols and cause a security exposure. Attackers can use various brute force techniques to access Azure VMs. Disable direct RDP and SSH access to your Azure Virtual Machines from the Internet.  
 
- Enable Azure Security Center:  Use Azure Security Center to prevent, detect, and respond to threats.  
 
- Securely extend your datacenter into Azure: To learn more about how to securely extend your datacenter into Azure, consult the link. 



## Next Steps 
Securing and Encrypting Data 
