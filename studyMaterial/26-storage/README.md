# 26. Cookies vs Local Storage vs Session Storage
## What are they?
JavaScript provides three mechanisms for storing data on the client − cookies, session storage, and local storage. Each one has advantages and disadvantages.

Local storage is the most recent mechanism. It allows for larger amounts of data to be stored, but the data is not deleted when the browser is closed. Local storage is useful for storing data that the user will need to access later, such as offline data.

Session storage is similar to cookies, but the data is only stored for the current session. This means that the data will be deleted when the user closes the browser. Session storage is useful for storing data that is sensitive, such as login credentials.

Cookies are the oldest and most well-known mechanism. They are simple to use and well supported by browsers. However, they are limited to 4KB of data and are often used to store data that is not sensitive, such as user preferences.

## Difference between Local Storage, Session Storage, and Cookies


|Local Storage|Session Storage|Cookies
|----------|----------|----------|
|It allows 10MB of data to be stored.|It allows 5MB of data to be stored.|The storage capacity is limited to 4KB of data.
|The stored data is not deleted when the browser is closed.|The data is stored only for the session and will be deleted when the browser is closed.|The data can be set to expire at a certain time.
|Local storage is useful for storing data that the user will need to access later, such as offline data.|Session storage is a great way to improve the performance of your web applications.|Cookies are a good choice for storing data that should not be persisted for a long time, such as session IDs.
|This is especially useful for storing data that you want to persist even if the user closes the browser, such as preferences or settings.|Session storage is useful for storing data that is sensitive, such as login credentials.|Cookies are often used to store data that is not sensitive, such as user preferences
|Local Storage is a new feature introduced in HTML5.|Session Storage is a new feature introduced in HTML5.|Cookies are the oldest (HTML4) and most wellknown mechanism.
|The data is not sent with the request from the client to the server.|The data is not sent with the request from the client to the server.|The data is sent with the request from the client to the server
}The data is stored on the browser and system.}|The data is stored on the browser only.|The data is stored on the browser only.

## Resources

https://dev.to/cotter/localstorage-vs-cookies-all-you-need-to-know-about-storing-jwt-tokens-securely-in-the-front-end-15id
https://www.makeuseof.com/session-local-storage-differences/
https://www.geeksforgeeks.org/difference-between-local-storage-session-storage-and-cookies/
https://www.tutorialspoint.com/difference-between-local-storage-session-storage-and-cookies-in-javascript
https://dev.to/iggredible/cookies-vs-local-storage-vs-session-storage-3gp3


