# 25. HTTP 2.0 vs HTTP 3.0 

Networks typically consider the OSI model or the TCP/IP model to define and organize their operation. These models, in turn, contemplate different layers, such as the network layer, the transport layer, and the application layer.

Each network layer has particular protocols that implement a myriad of functionalities. Examples are the IP at the network layer, TCP and UDP at the transport layer, and HTTP at the application layer.

These protocols evolve, thus being updated and extended over time. So, it is natural that network protocols have multiple versions.

## HTTP Version 2.0
HTTP version 2.0 was officially released in 2015, about eighteen years after the HTTP 1.1. Particularly, HTTP 2.0 focused on improving the protocol performance.

To do that, HTTP 2.0 implemented several features to improve connections and data exchange. Let’s see some of them:

Request multiplexing: HTTP 1.1 is a sequential protocol. So, we can send a single request at a time. HTTP 2.0, in turn, allows to send requests and receive responses asynchronously. In this way, we can do multiple requests at the same time using a single connection
Request prioritization: with HTTP 2.0, we can set a numeric prioritization in a batch of requests. Thus, we can be explicit in which order we expect the responses, such as getting a webpage CSS before its JS files
Automatic compressing: in the previous version of HTTP (1.1), we must explicitly require the compression of requests and responses. HTTP 2.0, however, executes a GZip compression automatically
Connection reset: a functionality that allows closing a connection between a server and a client for some reason, thus immediately opening a new one
Server push: to avoid a server receiving lots of requests, HTTP 2.0 introduced a server push functionality. With that, the server tries to predict the resources that will be requested soon. So, the server proactively pushes these resources to the client cache
Furthermore, HTTP 2.0 became a binary protocol, replacing the previous HTTP plain text versions. In summary, we can see HTTP 2.0 as a patch of enhancements to solve the problems and limitations of the last HTTP versions.

## HTTP Version 3.0
HTTP 3.0 is an Internet-Draft, different from the previous HTTP versions, which were/are Request For Comments (RFC) documents of the Internet Engineering Task Force (IETF). Its first draft was published in 2020.

The main difference between HTTP 2.0 and HTTP 3.0 is the employed transport layer protocol. In HTTP 2.0, we have TCP connections with or not TLS (HTTPS and HTTP). HTTP 3.0, in turn, is designed over QUIC (Quick UDP Internet Connections).

QUIC, in short, is a transport layer protocol with native multiplexing and built-in encryption. QUIC provides a quick handshake process, besides being able to mitigate latency problems in lossy and slow connections.

In addition to the potential benefits inherited from QUIC, another relevant characteristic of HTTP 3.0 is that it always creates encrypted connections. So, it is similar to always employing HTTPS in current HTTP 2.0.

## Summary
Currently, HTTP is a really relevant protocol, supporting multiple systems executing on the Internet. First released in 1991, this protocol had several updates, going through several versions.

From the first release (version 0.9) to the release of HTTP 2.0, we had multiple enhancements on the functionalities of HTTP, besides extensions in the protocol to add new methods and features.

Examples of such enhancements and novelties were the protocol header (1.0), status codes (1.0), persistent connections (1.1), request multiplexing (2.0), and server push (2.0).
 
Besides the new features previously cited, we also had the introduction of new methods in addition to the standard GET: POST (1.0), HEAD (1.0), PUT (1.1), PATCH (1.1), DELETE (1.1), CONNECT (1.1), TRACE (1.1), and OPTIONS (1.1).

In HTTP 3.0, however, the main novelty here is not a particular new feature. Actually, HTTP 3.0 replaces the transport layer protocol employed by HTTP from its first version, TCP, with a new one: QUIC.

By replacing TCP with QUIC, the HTTP developers expect, among other improvements, to achieve native and standard encryption (there are no more HTTP and HTTPS, every HTTP communication is encrypted) and fast establishment of connections.

Resources

https://www.makeuseof.com/what-is-http3-how-compare-http2/
https://http3-explained.haxx.se/en/why-quic/why-h2
https://www.geeksforgeeks.org/tcp-ip-model/
https://www.baeldung.com/cs/osi-model
https://ably.com/topic/http-2-vs-http-3

