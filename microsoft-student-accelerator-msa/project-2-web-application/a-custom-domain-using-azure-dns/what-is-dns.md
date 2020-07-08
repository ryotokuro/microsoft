# What is  DNS?

A **Domain Name Server** \(DNS\) is a **protocol** that falls under TCP/IP \(Transmission/Internet Protocol\). Put simply, DNS takes a **human-readable URL** like [`https://blonded.co/`](https://blonded.co/) and converts it into **an associated and known IP address** so that servers can interpret it. This is because computers and network devices use IP addresses as a form of **identification** to determine what is what.

Just as each device has their own unique IP Address, websites also have their identity expressed as a set of numbers in a form similar to `192.100.1`. So whenever you visit a website, it first visits a DNS to **ask for directions** to where it should go by giving it the human-readable domain name.

In this case, Microsoft is part of a DNS network that **looks up the IP address** in a **global directory** so it knows where to send you. It provides this service through Azure DNS, which specifically handles domains under the Azure name server.

## How does DNS work?

A DNS Server will do **two things**:

* maintain a local cache
* maintain a key-value database of domain-ip pairings

### Maintain a local cache

Maintain a **local cache** of **recently accessed domain names** and their associated IP addresses. This is so the DNS can **respond quickly** with a local **lookup request**. You can see this where it usually takes less time to connect to a website the second time in a row than it did when you first visited the website. Now if a DNS is unable to locate the information you're looking for \(if it can't find a match for the provided domain name\), then it will **pass down the request to another DNS server**. This handshake will keep on going until either a match is found, or the request times out. So if you give it a domain that doesn't exist, it will eventually time out \(hence directing you to an error\)

### Maintain a key-value pair database

The DNS will maintain a set of key-value pairs \(domain name -&gt; ip addresses\) that the DNS has **authority over**. So in this example, Azure DNS will have authority over applications hosted on the Azure server \(like my website\).

## DNS Servers are bound by location

Depending on where you're connected to the Internet, you are **assigned to different DNS servers**. If you're accessing a website from **on-premises**, ****you follow the DNS settings on your server. On the other hand, if you're connecting from an **external location** like a hotel, the DNS settings will **come from the Internet Service provider \(ISP\)** like Telstra or ADSL.

{% hint style="info" %}
On premises = DNS Settings from the server

External \(off premises\) = DNS from ISP
{% endhint %}

### Resolving a domain name request

A DNS takes a very methodical approach to resolving a request. The DNS follows a sequence of steps that goes from **cache**, to the **wider network** to raising an **exception**.

1. **Check the cache** to see if the domain name is stored. If so, then it uses it to fulfil the request
2. If it's not in the cache, the domain name will **contact other servers** to see if they have anything. It will continue doing so, and once a match has been found, the DNS will receive the response, **store the pair in its local cache** \(for future\) **and resolve the request**
3. In the else case where nothing can be found after checking the cache and asking around, the DNS Server will respond with a **404 Error: Domain not found**

## **IPv4 and IPv6**

As noted previously, every device connected to a network will have an IP address. This IP address will be unique to a given domain \(so your network will have one IP address usually\). With IP addresses, you essentially have **two standards** that they fall into: **IPv4** or **IPv6**.



\*\*\*\*

