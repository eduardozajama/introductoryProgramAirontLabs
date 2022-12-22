# 17. Fetch API. AJAX (XHR)

## What are Ajax and XHR?
### Ajax 
Stands for Asynchronous Javascript and XML. Ajax is a programming technique that allows us to create dynamic, complex, and asynchronous web applications. Ajax allows us to send and receive data from the webserver asynchronously without interfering with the current state or behavior of the web page or application.

### XHR 
Is the XMLHttpRequest Object which interacts with the server. Ajax technique in the nutshell leverages the XHR request to send and receive data from the webserver. This object is provided by the browser’s javascript environment. It transfers the data between the web browser and server.

### XMLHttpRequest
Before JSON took over the world, the primary format of data exchange was XML. XMLHttpRequest() is a JavaScript function that made it possible to fetch data from APIs that returned XML data.

XMLHttpRequest gave us the option to fetch XML data from the backend without reloading the entire page.

This function has grown from its initial days of being XML only. Now it supports other data formats like JSON and plaintext.
>[Create a XMLHttpRequest object](https://blog.loginradius.com/engineering/ajax-and-xhr-using-plain-javascript/#create-a-xmlhttprequest-object-) 

## Using the Fetch API
The Fetch API provides a JavaScript interface for accessing and manipulating parts of the protocol, such as requests and responses. It also provides a global fetch() method that provides an easy, logical way to fetch resources asynchronously across the network.

This kind of functionality was previously achieved using XMLHttpRequest. Fetch provides a better alternative that can be easily used by other technologies such as Service Workers. Fetch also provides a single logical place to define other HTTP-related concepts such as CORS and extensions to HTTP.

The Fetch API is a simpler, easy-to-use version of XMLHttpRequest to consume resources asynchronously. Fetch lets you work with REST APIs with additional options like caching data, reading streaming responses, and more.

The major difference is that Fetch works with promises, not callbacks. JavaScript developers have been moving away from callbacks after the introduction of promises.

For a complex application, you might easily get into a habit of writing callbacks leading to callback hell.

With promises, it is easy to write and handle asynchronous requests.

A basic fetch request is really simple to set up. Have a look at the following code:
```javascript
fetch('http://example.com/movies.json')
  .then((response) => response.json())
  .then((data) => console.log(data));
```
## Resources
>[Blog](https://blog.loginradius.com/engineering/ajax-and-xhr-using-plain-javascript/#create-a-xmlhttprequest-object-)

>[w3shools](https://www.freecodecamp.org/news/javascript-fetch-api-tutorial-with-js-fetch-post-and-header-examples/)

>[Mozilla Dev](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)


