# Workshop 2

## Contact Information

{% hint style="info" %}
**Speaker**  
Stephane Budo  
****sbudo@vigilant.it
{% endhint %}

## Networking

### Azure Virtual Networks \(V-Nets\)

* create private networks in the Cloud \(Azure\)

    ○ can control IP addresses

    ○ DNS servers

    ○ Security rules

    ○ Traffic flows

It's privatised

* has a private IP
* can be broken into subnets

    ○ break the one IP address into different sections

**Naming Rules for Vnets**

* Vnets need a UNIQUE NAME within it's own resource group
* Important to stick to a naming CONVENTION across resources

### Regions

* The Vnet is located inside a datacenter \(within a specific region\)
* Any resources you wish to connect, must be in the same region

### Subscriptions

You can create multiple vnets per subscription and per region

* Note: there is a limit
* Also you can create multiple subnets

### IP Addresses

* You can assign IP address to your resources if you want them to talk to each other or go to the internet

#### **Public IP addresses**

* Used to communicate with the Internet

#### Private IP addresses

* can't be used outside of your enclosed vnet

  Used to communicate within the VNet

## Connectivity

### Vnet to Vnet \(Vnet PEERING\) \(like P2P Bittorrent\)

* Connecting a Vnet with another Vnet
* Danger: they cannot have the same IP address because of CONFLICT

Vnet peering - connecting Vnets within the same Azure region GLOBAL Vnet peering - connecting Vnets across Azure regions

* Costs big bucks $$$$

They connect to multiple Vnets

* they're not transitive
* So if V1-V2-V3, V3 doesn't know about V1

### VPN Connections

What if you wanted to connect a Vnet outside of Azure???

* Use the gateway within Azure to get out

    ○ Created using a SUBNET gateway within Azure

    ○ Always created in pairs \(for high availibility\)

* Gateway in your target destination

### Types of Connections

1. Point-To-Site \(VPN\)
2. Site-To-Site \(VPN\) a. Go from a site b. Out through to a gateway within Azure c. To the Azure Vnet through the Vnet gateway
3. ExpressRoute \(Private Site-To-Site\) a. Don't go over the Internet unlike VPNs b. Create private connection between data centers and infrastructure on your environment

You can hybrid and use ExpressRoute where you need and VPN in other areas

## Network Services

### Azure DNS \(Domain Name Resolution\)

* you can set up DNS servers
* allow mapping from domain names to IP addresses

Private IP Addresses

* by default its configured by Azure-managed DNS
* They provide internal name resolution within your network

## CDNs \(Content Distribution\)

Caching content depending on the user location

* saved in the nearest server

## Load Balancing

Azure Load Balancer

* Balance load depending on the network traffic
* The important things for your server is to have high availability and resiliency

    ○ Having high uptime according to your SLA

    ○ How your network will react to failure

  ```text
    § High resiliency = being able to redirect traffic if something breaks
  ```

Public

* Maps public IP address and port number of incoming traffic

    ○ Maps to private IP address and port

* Interfaces between public IP and the IP within your own network

Internal \(Private\)

* Directs traffic inside the internal network
* Handles IPs inside your network

Internally, this is where Tiering occurs

* Load balancers are used to prioritise performance and traffic distribution within your network
* A good example use is when developing websites:

    ○ You usually have a web tier

    ○ and a backend tier \(this is usually on its own network\)

## Traffic Manager

