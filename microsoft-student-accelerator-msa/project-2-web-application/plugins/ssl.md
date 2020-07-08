# SSL

## Why do we need SSL?

SSL is essential for websites in order to **protect sensitive information** as it travels through the Internet. In particular, since you use the Internet to access websites, traffic that travels through websites is **susceptible to being attacked** \(whether it be listened in on, modified, etc\). SSL is therefore necessary to prevent these malicious attacks from occuring as you surf the net.

What SSL does essentially is that it takes the information that you're receiving and transmitting and **encrypts those messages** so that **only the intended recipients are able to access them**. Just like you wouldn't want a message you're sending to your best friend being read by your grandparents, SSL protects strangers from accessing your information when it travels across different computers \(since the Internet is basically a network of computers\).

Without SSL, you're basically exposed such that any sensitive information like your **credit card number, usernames, passwords** are vulnerable when it isn't encrypted. If you've ever visited websites without that little padlock next to the URL, any information you enter on that website can be viewed by the website authority!

So SSL provides a **network of trust** where websites are required to be verified before they can be assigned a certificate of trust. Large "trustworthy" organisations act as Certificate Authorities \(CAs\) to audit websites on their security to make sure the owners are valid \(authenticating them\) so that you can rest easy when you visit their website.

## Activating SSL

To activate SSL it's extremely to do so using Simple SSL. Since our website was created using Microsoft Azure, our certificate should be issued by our relevant certificate authority \(CA\), that is, **Microsoft IT**. As such, the process is essentially automated and a simple activation enables SSL on the website as seen below.

![Enabling SSL using Simple SSL](../../../.gitbook/assets/image%20%2895%29.png)

## Certificate Verification

To view the certificate on any browser, you can simply click the **lock icon next to the URL bar** and click on the 'Certificate' option. This allows me to see some basic information about the ticket including its **intended purpose, issuer and validation date**.

![Accessing the certificate through a browser](../../../.gitbook/assets/image%20%2896%29.png)

![Certificate shown through browser \(Chrome\)](../../../.gitbook/assets/image%20%2899%29.png)

## Mixed Content Filter

### Evaluation using SSL Labs

Using [SSL Labs](https://www.ssllabs.com/ssltest/index.html) I can do **deep analysis** on my current web SSL configuration to see if it was set up properly and compare it to other websites. The website will essentially measure the website against a set of **best practices** and verify the configuration is adhering to certain security standards.

After running my website through the filter, it came out with an overall rating of A \(sufficient, not quite A++\). It looks like my **key exchange and cipher strength are quite weak**, which could be due to the protocol my website is using not being the best available.

![Website received an A Star security rating](../../../.gitbook/assets/image%20%2898%29.png)

### Digging into the details

Going into the exact certificate details, we can look at the information listed to gain a better understanding of our exact configuration.

Here we can see the certificate is generated with **RSA 2048** encrypted using **SHA256** \(RSA being the key exchange and SHA256 being the encryption algorithm\). This means that our encryption method by current standards is quite good as these modes are common and not yet broken.

Moreover, we can see the **expiry date of the certificate** \(basically when I have to renew it\) and see it lasts for 1 year and 2 months until 24 Sep 2021. Additionally, the **Issuer** is also listed here so I can verify that the Certificate Authority at Microsoft IT did in fact issue this certificate. This certificate is therefore trusted across different supported browsers \(since Microsoft is a trusted CA\), which would mean the **SSL applies cross-browser on standard browers.**

![Certificate \#1 Analysis](../../../.gitbook/assets/image%20%28102%29.png)



