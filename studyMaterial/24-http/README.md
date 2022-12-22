# 24. HTTP

## Definition of HTTP
HTTP (Hypertext Transfer Protocol) is the base of the data communication for the web this is how the internet works when it comes to delivering the web pages. It is TCP/IP based protocol and things like text, audio, videos, images can be transmitted through it.

HTTP works on request and response cycle where the client requests a web page. Suppose, if you browse to google.com, you are requesting a web page from the server, and the server will deliver you response.

HTTP is a stateless protocol which means every single transaction you made through HTTP is independent in nature. However, this can be delivered through using HTTP cookies, server side sessions, variables, URL rewriting.

When a client wants to browse a website first thing that happens is that request is sent to the server known as HTTP message. Thereafter, the server will prepare a response and send it back. The message will be different depending on its message response and request.

## Request HTTP Message
![Request HTTP Message](/studyMaterial/24-http/resmsg.jpg)


1. Start line contains method, URI, and HTTP version.
Method: It is like a command that is given to the servers so that server will know what to do. for example, GET, POST, HEAD,
PUT, DELETE, etc.
URI: It expands to Uniform Resource Identifier is a set of readable characters and a way to locate the resource.
HTTP version: It specifies the version of HTTP a client is using.
2. In the headers, we have informational rules such as:
Host: Specifies the address of the server where we are sending a request.
Accept: Specifies the file type we are requesting.
Accept language: Specifies the language.
3. It doesn’t contain body in the request.

## Response HTTP Message
![Response HTTP Message](/studyMaterial/24-http/reqmsg2.jpg)
1. Start line: there is no method in the start line as it is only used in the request. In the response, we have the HTTP version and status code.
HTTP version: It specifies the version of HTTP a client is using.
Status code: It tells the client if the request succeeded or failed. for example, 404- page not found, 200 – ok, etc.
2. The header will contain the same information as the request.
Host: Specifies the address of the server where we a request is sent.
Accept: Specifies the requested file type.
Accept language: Specifies the language.
3. The body will hold the file we have sought.

The main issue of HTTP is that it is not encrypted and plain text is used, meaning that it is unsecured at transferring data among the computer and server. It is popular to exploit the man-in-the-middle attacks, if you run a HTTP connection anyone can put himself in the middle and start using names, emails, passwords in the plain text.

## HTTP response status codes
HTTP response status codes indicate whether a specific HTTP request has been successfully completed. Responses are grouped in five classes:

### Informational responses (100 – 199)
### Successful responses (200 – 299)
### Redirection messages (300 – 399)
### Client error responses (400 – 499)
### Server error responses (500 – 599)

>[Status Codes in detail](https://www.semrush.com/blog/http-status-codes/?kw=&cmp=LM_SRCH_DSA_Blog_EN&label=dsa_pagefeed&Network=g&Device=c&utm_content=622526966305&kwid=dsa-1754723155433&cmpid=18364824154&agpid=146618527572&BU=Core&extid=60109657981&adpos=&gclid=Cj0KCQiAtICdBhCLARIsALUBFcFX3TeqjJqNVflsJIjLGtuLaZ2DNxbL35PhlMlASYSENjIYqBgcYi8aAi3YEALw_wcB)

## HTTP Methods
>[HTTP Methods](https://www.tutorialspoint.com/http/pdf/http_methods.pdf)

# HTTP and Session Management
HTTP is designed as a stateless protocol, which means web servers do not maintain any information about the previous request. It has no memory of whether a user has just logged in the application. Modern web applications require maintaining the state of authentication and authorization during the user access of the application. This is accomplished by the session management capabilities that track the state of login and possibly other data, i.e., login name.

The state of login is commonly recorded in the memory of the web server, and a pointer to the memory location is sent to the browser. This memory location or name is called a session ID or a session token. Browsers typically use cookies to store the session ID.

>[Session Management](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html)

## Resources
https://www.semrush.com/blog/http-status-codes/?kw=&cmp=LM_SRCH_DSA_Blog_EN&label=dsa_pagefeed&Network=g&Device=c&utm_content=622526966305&kwid=dsa-1754723155433&cmpid=18364824154&agpid=146618527572&BU=Core&extid=60109657981&adpos=&gclid=Cj0KCQiAtICdBhCLARIsALUBFcFX3TeqjJqNVflsJIjLGtuLaZ2DNxbL35PhlMlASYSENjIYqBgcYi8aAi3YEALw_wcB 
https://developer.mozilla.org/en-US/docs/Web/HTTP/Status 

https://techdifferences.com/difference-between-http-and-https.html
https://www.tutorialsmate.com/2020/07/http-vs-https.html

https://www.dinosec.com/docs/OWASP_Session_Management_Cheat_Sheet_v2.0.pdfResources


https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html

https://www.coveros.com/understanding-session-management-one-of-owasp-top-10-part-1/



