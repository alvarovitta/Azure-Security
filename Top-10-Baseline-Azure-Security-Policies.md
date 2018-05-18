
Use the following guidance as described in this section to configure the top 10 baseline security policies you should start with in Azure . As your organization security and compliance evolves, more azure policies will need to be implemented.  


  


  


Guidance  


Use the information in the table below as a guideline when creating Azure policies. The table contains the top 10 Azure built-in policies you can use to begin defining your policies. 


  







Policy  
 


Definition  
 


Scope  
 


Parameters  
 



Enforce Tag and its Value  
 


Requires a tag and a value to be applied to a resource   
 


Apply to resources within Resource Group  
 


Example: costCode, businessowner, vmRole, compositeApp, vmWorkload, deploymentStage  
 



Enforce Allowed Locations  
 


Ensures that only approved locations are used when deploying resources to a region  
 


Apply to subscription or to Resource Group  
 


Example: Canada Central, Canada East  
 



Enforce Not Allowed Types  
 


This policy prohibits the deployment of specified resource types. Specify an array of the resource types to block  
 


Applies to whatever Resource Group that contains references that you do not you do not want to be accessible through the internet  
 


Example: Microsoft.network/PublicIPAddresses  
 



Monitor VM Vulnerabilities in Security Center [Preview]  
 


Monitors vulnerabilities detected by vulnerability assessment solution and VMs without a vulnerability assessment solution in Azure Security Center as recommendations.  
 


Subscription  
 


N/A  
 



Monitor Unprotected Web Application in Security Center [Preview]  
 


Web applications without a web application firewall protection will be monitored  by Azure security center as recommendations  
 


Subscription  
 


N/A  
 



Monitor Permissive Network Access in Security Center [Preview]  
 


Network security groups with rules that are too permissive will be monitored by Azure security center as recommendations  
 


Subscription  
 


N/A  
 



Monitor Missing System Updates [Preview]  
 


Missing security system updates on your servers will be monitored by Azure security center as recommendations.  
 


Subscription  
 


N/A  
 



Monitor Unprotected Network Endpoints [Preview]  
 


Network endpoints without Next Generation firewall protection will be monitored by Azure security center as recommendations.  
 


Subscription  
 


N/A  
 



Monitor Missing Endpoint Protection [Preview]  
 


Servers installed without an installed endpoint protection agent will be monitored by Azure security center as recommendations  
 


Subscription  
 


N/A  
 



Monitor OS Vulnerabilities OS [Preview]  
 


Servers which do not satisfy the configured baseline will be monitored by Azure security center as recommendations  
 


Subscription  
 


N/A  
 


  


  


  


Procedure:  How to deploy a Geo-compliant/Data Sovereignty baseline policy    


  


Use this procedure to build a baseline policy based on geographical or sovereign considerations.  


  


Available Azure Regions:   

australiaeast, australiasoutheast  


Brazilsouth  


canadacentral, canadaeast, centralus, centralindia  


eastus, eastus2, eastasia  


japanwest, japaneast  


koreacentral, koreasouth,  


Northeurope, northcentralus  


southcentralus, southindia, southeastasia  


uksouth, ukwest  


westus, westcentralus, westus2, westeurope, westindia,   



  

Access the policy definition  



Azure Quickstart > Azure Policy > Samples > Allowed Locations  


  

Deploy the policy to Azure  



Use:  Azure Template | PowerShell | Azure CLI  


  

Assign the policy  



Use PowerShell  


  

Define the policy parameters  



Use the following parameter values:  


-PolicyParameters canadacentral, canadaeast, centralus, eastus, eastus2,westus, northcentralus, southcentralus, westcentralus,  
 westus2  


  


  


  


Procedure:  How to deploy a cost management baseline policy   


  


Use this procedure to build a baseline policy based on cost management.  


   

Access the policy definition  



Azure Quickstart > Azure Policy > Samples > Not Allowed Resource Types  


  

Deploy the policy to Azure  



Use:  Azure Template | PowerShell | Azure CLI  


  

Assign the policy  



Use PowerShell  


  

Define the policy parameters  



Use the following parameter values:  


-PolicyParameters  Standard_G1, Standard_G2,Standard_G3, Standard_G4, Standard_G5, Standard_GS1, Standard_GS2,  
 Standard_GS3, Standard_GS4, Standard_GS5, Standard_GS5-8, Standard_GS5-16, Microsoft.HDInsight/clusters  


Note: Available VMs: get-azurevmsize <location>  


   


  


Procedure:  How to deploy a required tags baseline policy   


  


Use this procedure to build a baseline policy based on required tags.  


  

Define the policy definition  



Azure Quickstart > Azure Policy > Samples > Enforce Tag  


  

Deploy the policy to Azure  



Use:  Azure Template | PowerShell | Azure CLI  


  

Assign the policy  



Use PowerShell  


  

Define the policy parameters  



Use the following parameter values:  


Name of required tag, Value of required tag  


   


  


Procedure:  How to enforce policy naming conventions  


  


Use this procedure to enforce naming conventions.  


  

Define the policy definition  



Azure Quickstart > Azure Policy > Samples > Enforce Tag  


  

Deploy the policy to Azure  



Use:  Azure Template | PowerShell | Azure CLI  


  

Assign the policy  



Use PowerShell  


  

Define the policy parameters  



Use the following parameter values:  Regular expression pattern  


  


Next Steps 


Securing your Azure Resources 
