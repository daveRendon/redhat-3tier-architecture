# Red Hat 3-tier Architecture
## Solution Overview 
This Azure Quick Start template deploys a 3 Tier Red Hat Solution on Azure.  The Solution includes Presentation Tier Web Servers, Application tier App Servers and Data Tier Database Servers running Red Hat Enterprise Linux 7.3. Template will build everything starting from Azure Infrastructure components to Red Hat VMs deployment. This template will deploy multiple number of VMs in each tier as per requirement. 

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FSpektraSystems%2Fredhat-3tier-architecture%2Fmaster%2Fazuredeploy.json?token=AUNpBhn83gtFTK0V9oB4C8mHTa8asYYmks5YnDJmwA%3D%3D" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FSpektraSystems%2Fredhat-3tier-architecture%2Fmasterhttps://raw.githubusercontent.com/SpektraSystems/redhat-3tier-architecture/master/azuredeploy.json?token=AUNpBgMRJaQ1TWrJyU8sNK3LbDlIUrbJks5YnDFwwA%3D%3D" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.png"/>
</a> 
 ?token=AUNpBhn83gtFTK0V9oB4C8mHTa8asYYmks5YnDJmwA%3D%3D
 
##Deployment Solution Architecture 

This template will deploy: 

- Four storage account 
-	One Virtual Network with four subnets
-	External Load Balancer to load balance all the Web VMs and to facilitate access to them.
- Internal Load Balancer to load balance all the App VMs.
-	2 Public IP’s, one for external Load balancer and other for Jump VM. 
-	3 Virtual Machine Availability sets for Presentation Tier, Application Tier and Data tier.
-	One Jump VM.
-	Two Red Hat Enterprise Linux VMs in each tier.

![Deployment Solution Architecture](https://github.com/SpektraSystems/redhat-3tier-architecture/blob/master/images/architecture.png?raw=true)

##Licenses and Costs 

The Red Hat Enterprise Linux 7.3 image used in this solution is the PAYG model and doesn't require the user to license it, it will be licensed automatically after the instance is launched first time. Use of this image carries a separate hourly charge that is in addition to Microsoft's Linux VM rates. Total price of the VM consists of the base Linux VM price (shown on the next pages) plus RHEL VM image surcharge.  Click [here](https://azure.microsoft.com/en-us/pricing/details/virtual-machines/red-hat/) for pricing details.

##Prerequisites 

- Azure Subscription with specified payment method (Red Hat Enterprise Linux is a market place product and requires payment method to be specified in Azure Subscription
-	User account with admin or contributor access to the given azure subscription

##Deployment Steps  

Build your Barracuda WAF environment on Azure in a few simple steps:  
- Launch the Template by click on Deploy on Azure.  
- Fill in all the required parameter values. Accept the terms and condition on click Purchase. The deployment takes about 4 minutes. 

##Post Deployment Steps 

After successful deployment, this template will output the IP address and FQDN of both external load balancer and Jump VM. User can access Web Tier VMs via external load balancer IP/FQDN and admin can access all VMs by logging into the Jump VM via Jump VM IP.

##Support 

For any support related questions or customization requirements, please contact info@spektrasystems.com



