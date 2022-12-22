# 23. HTTPS
## What is HTTPS?
### Definition of HTTPS
HTTPS (Hypertext Transfer Protocol Secure) is nothing but the HTTP working in tandem with SSL (Secure Socket Layer) that is the “S” in HTTPS. SSL takes care of ensuring that the data goes securely over the internet. The alternative names given to HTTPS are HTTP over TLS, HTTP over SSL and HTTP secure.

This protocol was designed to increase primarily on the internet when communicating with web sites and sending sensitive data. This made man-in-the-middle attack increasingly difficult as the data send is no longer in plain text.

To secure your website one needs to purchase something called SSL certificate. These are relatively expensive and most hosting companies offer them. SSL certificate is analogous to an online identification card. SSL certificate also encrypts any data that passes through https protocol.

Now, a client requests data from the server it looks for the SSL certificate which will verify websites identity with the certificate. If everything is good, a handshake takes place where an encryption method is decided through SSL.


## Differences between HTTP and HTTPS
| BASIS FOR COMPARISON |HTTP | HTTPS
| ----------- | ----------- | ----------- |
|Prefix Used|Url begins with "http://"|Url begins with "https://"
|Security| Unsecured.| Secured.
|Operated On |Application layer|Transport layer.
|Encryption |No encryption is there|Encryption is used.
|Certificate|Not required.|Necessary
|Port Used|Port number 80 is used for communication.|Port number 443 is used for communication.
|Characteristics|It is subject to man-in-the-middle and eavesdropping attacks.|It is designed to resist man-in-the-middle and eavesdropping attacks and is considered secure against such attacks.
|Example|Websites like internet forums, educational sites.|Websites like Banking Websites, Payment gateway, Shopping Websites, etc.

# Types of TLS/SSL Certificate
There are two classifications of TLS/SSL certificates:-
1. Based on the number of domains or subdomains to support:
Single Domain or Single Name – one certificate secures only a single domain or an individual subdomain. For example, if you buy a certificate to secure www.abc.com, you cannot use the same certificate to secure its subdomain help.abc.com.

Wildcard – one certificate secures a single domain and all the subdomains under it. Websites with wildcard certificate have an asterix (*) and a period before their domain names. For example, a domain secured by a wildcard certificate is denoted by https://*.abc.com, where the ‘*’ can be any of abc.com’s subdomains like help.abc.com, blog.abc.com, etc.

Multi-domain or Subject Alternative Name (SAN) – one certificate secures a number of domains and subdomains. Eg. An SAN certificate used to secure www.abc.com can secure www.abc.org, www.abc.co.us, blog.abc.com, etc.


2. Based on the level of assurance needed:
Domain Validation (DV) – these TLS/SSL certificates are the easiest to obtain. The URL of websites with DV TLS/SSL certificates will have only the HTTPS and padlock and not the business name. Hence, there’s no way for visitors to check if the website really belongs to the business they’re looking for, despite the secure sign. DV TLS/SSL certificates can be got in minutes with no business verification.

Organization Validation (OV) – OV TLS/SSL certificates are used by organizations that deal with sensitive customer data. Websites with OV TLS/SSL certificates have their business name on the address bar along with HTTPS and the padlock. Since these certificates offer high assurance, they’re provided only after appropriate scrutiny by the CAs, are more expensive, and can take day to issue.

Extended Validation (EV) – EV TLS/SSL certificates offer the highest level of security and are the hardest to obtain. To get an EV certificate, the organization has to undergo rigorous vetting by the CA, which includes verifying the physical existence of the business. Websites with an EV TLS/SSL certificate have their organization name, country code, and padlock in green. These certificates are very expensive and can take up to 3 days to issue.

All these certificates are issued on completion of DCV (Domain Control Validation), wherein the organization has to prove that the domain they’re requesting certification for really belongs to them.

## SSL vs TLS
Without getting too technical, the main difference between SSL and TLS is how they establish secure connections. Both do it through a process known as “the handshake”, which is how the server and the client authenticate each other before finally creating an encrypted connection. The SSL handshake is quite different to the TLS handshake. 

The SSL version involves using a port to make what is known as an explicit connection. TLS, on the other hand, connects via a protocol, which is known as an implicit connection. The process of both SSL and TLS handshakes is dictated by something known as cipher suites, algorithms that outline the sequence of steps that must be performed in order to execute a cryptographic function. (You can read more about cipher suites here). The cipher suites used by SSL and TLS are very different, with TLS-supported cipher suites being faster and more secure than those supported by SSL. 

Note: While the SSL protocol and the TLS protocol are not the same thing, SSL certificates and TLS certificates do refer to the same thing. It is a digital certificate you install on your server so that web browsers can connect with your site via HTTPS. All modern SSL certificates should work by doing this via the TLS protocol. To ensure that your website is configured to use the latest version of TLS, check your server settings.




## Resources

>[Blog](https://www.venafi.com/blog/what-are-differences-between-http-https-0)
>[Hostinger](https://www.hostinger.com/tutorials/http-vs-https)
>[Javatpoint](https://www.javatpoint.com/http-vs-https)

