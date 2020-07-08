# Introduction

So the whole point here is to use Azure DNS so that we have everything instantiated by Azure. Essentially we use Azure DNS to **host our DNS records** to redirect our new domain to the same website. Then whenever someone navigates to the new and improved url, it will take them to my website.

What Azure DNS is essentially doing is helping to **resolve the IP address of the web server with the actual domain that people access the website through**. For example, whenever you type in the url [https://www.animal-crossing.com/](https://www.animal-crossing.com/), there is a DNS \(Domain Name Server\) which contains a table to match the url to its associated IP address. You might picture it being something like below:

| URL \(Domain Name\_ | Website IP Address |
| :--- | :--- |
| [https://www.animal-crossing.com/](https://www.animal-crossing.com/) | 123.52.51 |
| [https://docs.microsoft.com/](https://docs.microsoft.com/) | 54.255.621 |
| [https://pizzahut.com/](https://pizzahut.com) | 221.434.444 |

So Azure DNS will essentially take my custom url \(let's say it's **https://msa.syd/** for now\) and direct it to the IP address associated with [https://msa-tai.azurewebsites.net/](https://msa-tai.azurewebsites.net/) so that both domains redirect to the same location \(my website\). So basically the "official domain name" is what I created in Azure but the Azure DNS will allow me to have a custom domain associated with it as an **alias**.

