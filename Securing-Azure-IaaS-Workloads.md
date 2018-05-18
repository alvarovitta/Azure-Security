
Security requirements can vary for different types of workloads.  When you move to Azure IaaS, you can apply your expertise in securing virtual environments and use a new set of options to help secure your assets. 


## Guidance 
- Implement Privileged Access Workstations (PAWs) that is protected from Internet attacks and threat vectors to complete sensitive tasks.  

- Use Multi-Factor authentication to safeguard access to data and applications while meeting user demand for a simple sign-in process.  
- Limit and constrain administrative access to ensure that you secure the accounts that manage your IaaS workloads. For example, you can use Privileged Identity Management to manage, monitor, and control access in your organization. It helps you remain aware of the actions that individuals take in your organization. It also brings just-in-time administration to Azure AD by introducing the concept of eligible admins.  
- Use DevTest labs for testing and development purposes because it uses Azure Role-Based Access Control (RBAC) to segregate duties into roles that grant only the level of access necessary for users to do their jobs. RBAC comes with predefined roles (owner, lab user, and contributor).  
- Control and limit endpoint access to minimize the risk of unauthorized access. You can use a VPN option (I.e. Site-to-Site) to reconfigure the access control lists on the NSGs to not allow access to management endpoints from the Internet. 
- Use a key management solution such as Azure Key Vault to securely store encryption keys and small secrets like passwords in hardware security module (HSM) for your Azure resources. 
- Use a centralized security management system such as  Security Center and Operations Management Suite Security and Compliance to monitor your servers for patching, configuration, events, and activities that might be considered security concerns 
- Manage your virtual machines by security hardening the operating systems, installing antimalware and installing the latest security updates 



## Next steps 
Securing PaaS Applications 
