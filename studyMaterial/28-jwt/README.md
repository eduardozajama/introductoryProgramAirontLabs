# 28. JWT

## What is JSON Web Token?
JWT is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with HMAC algorithm) or a public/private key pair using RSA.

Let’s explain some concepts of this definition further.

Compact: Because of its size, it can be sent through an URL, POST parameter, or inside an HTTP header. Additionally, due to its size its transmission is fast.
Self-contained: The payload contains all the required information about the user, to avoid querying the database more than once.

## When should you use JSON Web Tokens?
These are some scenarios where JSON Web Tokens are useful:

### Authentication
 This is the typical scenario for using JWT, once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used among systems of different domains.
### Information Exchange
 JWTs are a good way of securely transmitting information between parties, because as they can be signed, for example using a public/private key pair, you can be sure that the sender is who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn’t changed.

### Authorization
 Once a user is successfully logged in, an application may request to access routes, services, or resources (e.g., APIs) on behalf of that user. To do so, in every request, it must pass an Access Token, which may be in the form of a JWT. Single Sign-on (SSO) widely uses JWT because of the small overhead of the format, and its ability to easily be used across different domains.
## Which is the JSON Web Token structure?
JWTs consist of three parts separated by dots (.), which are:

Header
Payload
Signature
Therefore, a JWT typically looks like the following.

Xxxxx.yyyyy.zzzzz


The JOSE (JSON Object Signing and Encryption) header contains the type of token — JWT in this case — and the signing algorithm.  

The JWT payload contains the claims. This is displayed as a JSON string, usually containing no more than a dozen fields to keep the JWT compact. This information is typically used by the server to verify that the user has permission to perform the action they are requesting.

There are no mandatory claims for a JWT, but overlaying standards may make claims mandatory. For example, when using JWT as bearer access token under OAuth2.0, iss, sub, aud, and exp must be present. some are more common than others. 

The JWT signature ensures that the token hasn’t been altered. The party that creates the JWT signs the header and payload with a secret that is known to both the issuer and receiver, or with a private key known only to the sender. When the token is used, the receiving party verifies that the header and payload match the signature. 

The output is three Base64 strings separated by dots that can be easily passed in HTML and HTTP environments, while being more compact compared to XML-based standards such as SAML.

The following shows a JWT that has the previous header and payload encoded and it is signed with a secret.

![JWT](/studyMaterial/28-jwt/encoded-jwt4.png)
To see for yourself what is inside a JWT, use the JWT.io Debugger It allows you to quickly check that a JWT is well formed and to manually inspect the values of the various claims.

>[JWT.io Debugger](https://jwt.io/?_gl=1*gkwass*rollup_ga*ODY4MTQ4NjYwLjE2NzE1NzEwMDg.*rollup_ga_F1G3E656YZ*MTY3MTU3MTAwOC4xLjEuMTY3MTU3MzMwNC42MC4wLjA.&_ga=2.98456863.1858683253.1671572541-868148660.1671571008)
## Resources
https://jwt.io/
https://auth0.com/learn/json-web-tokens
https://www.akana.com/blog/what-is-jwt
https://dev.to/cotter/localstorage-vs-cookies-all-you-need-to-know-about-storing-jwt-tokens-securely-in-the-front-end-15id
https://auth0.com/docs/secure/tokens/json-web-tokens/json-web-token-structure

