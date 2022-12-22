# 29. JSONP & CORS

For security reasons, web browsers prevent what are called “cross-origin” or “cross-site” requests from one domain to another. JavaScript XMLHTTPRequests (commonly called “AJAX” requests) inherit all of the authentication context of the currently logged in user, so a malicious web page could attempt to make malicious requests that cross domain contexts and cause trouble. Historically, that has made it difficult for web developers to build web applications making use of third-party APIs.

Fortunately, techniques have since been developed that allow developers to securely access APIs cross-domain. The two most popular ones are CORS and JSONP.

## What is CORS?
CORS is an acronym for Cross-Origin Resource Sharing.

Consider you have a website named abc.com and you want to make a request to your another website named xyz.com. In JSON, you won’t be allowed to do so and you will end up with a CORS message as in the image below.
![](/studyMaterial/29-jsonpAndCors/cors.jpg)
A request made from a script on the website on one domain (say abc.com) to a website on a different domain (say xyz.com) is referred to as a Cross-Origin Request.

For security reasons, a Cross-Origin request is blocked by the browsers to prevent hackers from getting access to your data. As a result, we get the Cross-Origin Request Blocked message as shown in the image above.
## What is JSONP?
JSON with Padding — JSONP for short — is a technique that allows developers to bypass the same-origin policy enforced by browsers by using the `<script> ` element’s nature. The policy disallows reading any responses sent by websites whose origins are different from the one currently used. Incidentally, the policy allows sending a request, but not reading one.
A website’s origin consists of three parts. First, there’s the URI scheme (i.e., https://), then the host name (i.e., logrocket.com), and, finally, the port (i.e., 443). Websites like http://logrocket.com and https://logrocket.com have two different origins due to the URI Scheme difference.

## Limitations of JSONP
JSONP, when executed over CORS, has the following limitations:

A JSONP request must be an HTTP GET request as we need to embed it in the <script> tag.
The response that we receive cannot be parsed and will be executed as-is by the browser.
There is no possible way to get the HTTP error codes when requesting JSONP data over cross-origin.

## Resources 

https://www.filecloud.com/blog/using-jsonp-for-cross-domain-requests/
https://www.w3schools.com/js/js_json_jsonp.asp
https://dev.socrata.com/docs/cors-and-jsonp.html
https://blog.logrocket.com/jsonp-demystified-what-it-is-and-why-it-exists/
https://medium.com/developers-arena/understanding-json-jsonp-cors-and-bypassing-cors-with-jsonp-fa5f0cc4edd4


