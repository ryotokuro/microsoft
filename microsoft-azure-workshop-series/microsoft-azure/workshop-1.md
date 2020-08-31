# Workshop 1

## Azure Resource Manager

The top 3 identity providers are Facebook, Amazon and Microsoft.

Azure Resource Manager provides tools to create and deploy resources with several different interacing options for interacting with the cloud:

* Azure Portal
* Command Line \(CLI\)

## Resource Providers

Resource providers are the categories in which resource managers are grouped in. As the user, you this is classified as Infrastructure as a Service \(IaaS\), giving you the options to utilise the following types of resources in the cloud:

* Compute
* Storage
* Networking

## Templates

Instead of having to deploy a set of resources and go through all the steps in the app configuration, you can **create a template to standardise the creation of resources to have consistency across all deployments within your organisation**.

## Azure Compute

### Virtual Machines

* Virtual machines are a software emulation of physical computer
* Users don't require the physical hardware

**Compute options \(the different types of VMs\)**

1. Burstable a. cheap
2. General purpose a. The 'D' series i. v2, v3 new versions
3. V series \(Compute Intensive\) a. SQL high compute power

## Regions

* What region it will be deployed in
* Available 99.95% of the time \(That's the SLA \(Service Level Agreement\)\)
* 99.99% time = 4 mins per month

## Virtual Networks

* VMs must use a Virtual Network

Resource group part of a dependency

### Required resources

* Network interfaces
* Public IP address
* Virtual network and subnets

### Additional resources

* Network Security Groups \(NSG\)
* Load Balancers

Availability Zones: resources deployed across different data centres \(HINT\)

### Availability Sets

* I want a VM in one domain and another domain
* Gives you a higher SLA

### Scale Sets

* Scale virtual machines up and down for demand
* You can deploy multiple virtual machines which are identical
* Scale sets help with load balancing and scale things automatically based on demand

Fold domain: when we're going to do maintenance, this is the hardware that we're taking offline

* i.e. fold domain example is a rack set

Type 1: normal VM Type 2: VM in a VM \(hypervisor 2\)

{% hint style="info" %}
**Hypervisors** are an **abstraction** of virtualisation
{% endhint %}

* There is an abstraction layer between the VM and the hardware

  e.g. VMWare

## Containers

### Hardware Virtualisation

* multiple hardwares running on a machine

Container virtualising application in it's own bubble

* runs on its own virtual machine
* or own hardware

So you can CONTAIN applications and run them on hardware

* so this becomes independent
* CLI:

    ○ create applications in containers

    ○ you can update them and deploy

Use a Docker Engine to run the hardware

Container is independent from the OS

* You can operate agile
* And iterate quickly
* You can scale and deploy it easily

### clustering

* run on hardware
* if it fails it will immediately instantiate it on another hardware

## Serverless Computing

Software as a Service \(Saas\) vs. PaaS

* runs without you having to worry about the service
* on the backend its connected to a database, etc

Webapps

E.g.

* Microsoft Flow
* Azure Logic Apps
* Azure functions

    ○ Can run through Powershell on different servers

    ○ Small pieces of code, easy to run

    ○ Deploy serverless apps on Azure

Azure App Service

* build and host web apps in language of choice
* Use whatever infrastructure you want

