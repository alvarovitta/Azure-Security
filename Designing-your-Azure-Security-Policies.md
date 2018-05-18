
Use this section to follow supplemental design and guidance on how implement Azure security policies. 


 


Design considerations: 

Keep organizational hierarchies in mind when creating definitions and assignments.  
 


To apply policies across subscriptions, you must have permissions across the subscriptions. 



 

Plan how to manage policy exceptions 



 


Guidance 

Create policy definitions at a higher level such as the management group or subscription level, and assigning at the next child level. For example, if you create a policy definition at the management group level, a policy assignment of that definition can be scoped down to a subscription level within that management group.  
 


Start with using an audit effect vs a deny effect when creating policy definitions in your environment. This technique will help you track the effects of your policy definition on the resources in your environment.  
 


 If you have scripts already in place to auto scale up your applications, setting a deny effect may hinder those automation tasks you already have in place.   
 


Use initiative definitions instead of policy definitions even for single policies. This technique helps with tracking.  
 


Apply policies that map to organizational compliance, operational and security requirements. 
 


Develop a process that justifies and manages exceptions to policies. 



 


 


Use the following tables to collect policy information so that you can create policies and definitions: 


 


Policy/Initiative definition 







Field 
 


Value 
 



Resource Policy or Initiative Name 
 


<policy or initiative name> 
 



Resource Policies* 
 


<set of policies included> 
 



Description 
 


 
 



Mode 
 


<all, indexed> 
 



Policy Parameters 
 


 
 



Policy Rule 
 


 
 



Effect 
 


<Audit, Deny, Append, AuditIfNotExists, DeployIfNotExists, DenyIfNotExists> 
 


*In the case of initiatives 


 


Policy/Initiative assignment 







Field 
 


Value 
 



Name 
 


<assignment name> 
 



Policy Definition 
 


<policy definition> (see above) 
 



Scope 
 


<subscription, resource group, resource> 
 



Exclude Scope 
 


 
 


 


Procedure: How to create and assign a resource policy 


 


Use this procedure to create and manage policies to enforce compliance. The Subscription Owner uses Azure Portal, PowerShell, or Azure CLI. Refer to Top 10 Baseline Azure Security Policies for recommended patterns 

Sign into the Azure portal 



Login as the Subscription Owner, see:  Azure Portal 


 


Create and manage policies to enforce compliance 

Create a policy to enforce compliance. Define the policy in terms of rules, scope, exceptions, and effect. 


Refer to the following: 

Assign a policy 


Implement a new custom policy 


Create a policy definition with PowerShell 




 


Procedure: How to create and assign an initiative policy definition  


 


Use this procedure to manage policies at scale, leverage initiatives. The Subscription Owner uses Azure Portal, PowerShell, or Azure CLI.  


 

Sign into the Azure portal 



Login as the Subscription Owner, see:  Azure Portal 


 

Create and manage policies to enforce compliance 



Create a policy to enforce compliance. Define the policy rules, scope, exceptions, and effect. 


Refer to the following: 

Initiative Assignment 



 


Next Steps 


Top 10 Baseline Azure Security Policies 
