# Azure DNS

Azure DNS lets you **host and manage your own domains** using the Azure infrastructure. This is a **name server** that Microsoft set in place such that Azure DNS can go and fetch records from these servers that contain information on the domain-ip mappings. What's great about this is that you can access all of this just by using your Azure login credentials, so you don't have to use any third-party tools to link anything up.

So essentially Azure DNS is the **Start of Authority** \(where computers contact to resolve the domain request\) for your domain. The only thing is that you **can't create a domain name using Azure DNS** - rather you need to do so using a **third party registrar** \(where you select your domain name and buy it\).

## Why use Azure DNS?

Azure DNS is hosted on the Azure Resource Manager, which means you can take advantage of the benefits that come with Azure RM. These benefits include:

* Improved security
* Ease of use
* Private DNS domains
* Alias record sets

### Security features

In terms of security for the DNS, Azure DNS also provides:

* **Role-based access control** - this means that you can assign roles to users within your resource group and control who can see/edit what. This is advantageous when you have an organisation or team managing different resources under a branch of Azure. 
* **Activity logs** - with this you can track any changes that happen to your resource, helping you maintain your system, recover critical points and identify errors when things occur. 
* **Resource locking** - finally, resource locking allows you to prevent access to certain resources completely, placing restrictions or limitations to things like resource groups or resources themselves.



