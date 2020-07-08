# SSL

## Why do we need SSL?

## Activating SSL

To activate SSL it's extremely to do so using Simple SSL. Since our website was created using Microsoft Azure, our certificate should be issued by our relevant certificate authority \(CA\), that is, **Microsoft IT**. As such, the process is essentially automated and a simple activation enables SSL on the website as seen below.

![Enabling SSL using Simple SSL](../../../.gitbook/assets/image%20%2893%29.png)

## Certificate Verification

![Certificate shown through browser \(Chrome\)](../../../.gitbook/assets/image%20%2896%29.png)

## Mixed Content Filter

### Evaluation using SSL Labs

Using [SSL Labs](https://www.ssllabs.com/ssltest/index.html) I can do **deep analysis** on my current web SSL configuration to see if it was set up properly and compare it to other websites. The website will essentially measure the website against a set of **best practices** and verify the configuration is adhering to certain security standards.

After running my website through the filter, it came out with an overall rating of A \(sufficient, not quite A++\). It looks like my **key exchange and cipher strength are quite weak**, which could be due to the protocol my website is using not being the best available.

![Website received an A Star security rating](../../../.gitbook/assets/image%20%2895%29.png)

### Digging into the details

Going into the exact certificate details, we can look at the information listed to gain a better understanding of our exact configuration.

Here we can see the certificate is generated with **RSA 2048** encrypted using **SHA256** \(RSA being the key exchange and SHA256 being the encryption algorithm\). This means that our encryption method by current standards is quite good as these modes are common and not yet broken.

Moreover, we can see the **expiry date of the certificate** \(basically when I have to renew it\) and see it lasts for 1 year and 2 months until 24 Sep 2021. Additionally, the **Issuer** is also listed here so I can verify that the Certificate Authority at Microsoft IT did in fact issue this certificate. This certificate is therefore trusted across different supported browsers \(since Microsoft is a trusted CA\), which would mean the **SSL applies cross-browser on standard browers.**

![Certificate \#1 Analysis](../../../.gitbook/assets/image%20%2898%29.png)



