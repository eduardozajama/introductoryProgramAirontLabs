# 27. SSO. OAuth 2.0

## Single Sign-On
Single Sign-on (SSO) occurs when a user logs in to one application and is then signed in to other applications automatically, regardless of the platform, technology, or domain the user is using. The user signs in only one time, hence the name of the feature (Single Sign-on).

For example, if you log in to a Google service such as Gmail, you are automatically authenticated to YouTube, AdSense, Google Analytics, and other Google apps. Likewise, if you log out of your Gmail or other Google apps, you are automatically logged out of all the apps; this is known as Single Logout.

SSO provides a seamless experience for users when using your applications and services. Instead of having to remember separate sets of credentials for each application or service, users can simply log in once and access your full suite of applications.

Whenever users go to a domain that requires authentication, they are redirected to the authentication domain where they may be asked to log in. If the user is already logged in at the authentication domain, they can be immediately redirected to the original domain without signing in again.

## How it works
Single Sign-on and Single Logout are possible through the use of sessions. There may be up to three different sessions for a user with SSO:

Local session maintained by the application

Authorization Server session, if SSO is enabled

Identity Provider (IdP) session, if the user chose to log in through an Identity Provider (such as Google, Facebook, or an enterprise SAML Identity Provider)

With SSO, a central domain performs authentication and then shares the session with other domains. The way a session is shared may differ between SSO protocols, but the general concept is the same.

For example, the authentication domain may generate a signed JSON Web Token (JWT) (encrypted using JSON Web Encryption (JWE)), which contains all the information needed to identify the user for any other domain requiring authentication. This token is passed to the client, but because it is signed, it cannot be modified in any way by the client. The token can be passed to the original domain by a redirect and used by the authentication domain and any other domains to identify the user.

Single sign-on solutions use the following steps to ensure a user's credentials are redirected from an SP to an IdP: 

1. The user accesses an SP, such as a website or application.
2. The SP sends an authentication token to the IdP, such as the SSO system.
3. The IdP sends an SSO response back to the SP.
4. The user will be prompted to log in.
5. When the user’s credentials are validated, they will be able to access other websites and applications from the SP without having to log in separately.
## What Is an Authentication Token?
When a user signs in to an SP using an SSO service, an authentication token that identifies the user is verified is created. An authentication token is digital information stored within the user’s browser or the SSO service’s servers.

Every application the user accesses will then check with the SSO service, which passes the token to the application to approve the request. Authentication tokens are passed back and forth between SPs and IdPs to share, confirm, and verify user identification information, such as their username, email address, and password. This is crucial to SSO protocols, which enable identity verification to occur away from other cloud services.

## How Are SAML and OAuth Used with SSO?
Authentication tokens use communication standards to ensure they are valid. The main standard is Security Assertion Markup Language (SAML), which is the language used to write authentication tokens. The SAML standard uses Extensible Markup Language (XML) to enable user authentication and authorization to be exchanged over secure domains. When used in SSO, SAML communicates between the user, an SP, and the IdP.

The process of securely providing users access to multiple services with just one login requires the user’s information to be authorized. This happens through open authorization (OAuth), which is a framework that enables a user’s account information to be used by various third-party services. When a user requests access to an application, the SP sends a request to the IdP, 
which then verifies and authenticates the request to grant the user access. A good example of this is choosing to use a Facebook account to sign in to a website instead of entering a username and password. 

OAuth and SAML are separate protocols that can both be used in conjunction with SSO. OAuth is used to authorize users while SAML authenticates users.
## How does OAuth work?
![](/studyMaterial/27-sso/oauth-2-flow-diagram.png)

>[Read more about OAuth](https://fullstackdeveloper.guru/2020/05/22/how-does-oauth-2-0-work/)

## Resources

https://spanning.com/blog/oauth-2-what-is-it-how-does-it-work/
https://darutk.medium.com/the-simplest-guide-to-oauth-2-0-8c71bd9a15bb
https://www.apisec.ai/blog/what-is-oauth
https://fullstackdeveloper.guru/2020/05/22/how-does-oauth-2-0-work/
https://www.fortinet.com/resources/cyberglossary/single-sign-on
https://auth0.com/docs/authenticate/single-sign-on#how-it-works



