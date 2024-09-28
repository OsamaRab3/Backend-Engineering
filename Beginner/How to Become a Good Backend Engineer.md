# How to Become a Good Backend Engineer (Fundamentals)


> In this video, I discuss the path of becoming a backend engineer through concepts and fundamentals. These are not tools 🧰 these are backend concepts and fundamentals technologies.  


## Table of Contents
- [Communication Protocols](#1-communication-protocols)
- [Web Servers](#2-web-servers)
- [Database Engineering](#3-database-engineering)
- [Proxies](#4-proxies)
- [Caching](#5-caching)
- [API Web Framework](#6-api-web-framework)
- [Message Formats](#7-message-formats)
- [Security](#8-security)


## 1. Communication Protocols

Communication protocols define the rules for exchanging data between servers, clients, and various devices over a network. Understanding these protocols is essential for backend developers, as they form the foundation of how web applications communicate.

### Common Communication Protocols in Web Development:
- **HTTP/HTTPS**: The HyperText Transfer Protocol (Secure) is the foundation for data communication on the web, allowing clients and servers to exchange web resources. HTTPS ensures secure, encrypted communication using SSL/TLS.
- **WebSockets**: A protocol providing full-duplex communication over a single TCP connection, enabling real-time data exchange, often used in chat applications or live updates.
- **TCP/IP**: The Transmission Control Protocol (TCP) and Internet Protocol (IP) suite is fundamental to transmitting data over the internet. TCP ensures reliable, ordered delivery of data between systems.

### Important Questions to Consider about Communication Protocols:
Hussein Nasser, in one of his videos, emphasized the importance of mastering communication protocols, particularly for backend development. Here are some of the critical questions you should be able to answer:

1. **How does HTTP work?**
   - Understand the request-response cycle in HTTP, including methods like GET, POST, PUT, DELETE, and how servers respond with status codes.
  
2. **What happens when you use TCP?**
   - Know how TCP establishes a connection using a three-way handshake (SYN, SYN-ACK, ACK) and how data is transmitted reliably with features like acknowledgment, retransmission, and flow control.

3. **Why is TCP sometimes considered slow?**
   - Be familiar with the concept of TCP’s overhead due to connection setup (handshakes), retransmission, congestion control, and the slow start mechanism.

4. **What is the difference between TCP and UDP?**
   - TCP is connection-oriented and reliable, while **UDP** (User Datagram Protocol) is connectionless and faster but does not guarantee delivery.

5. **How does SSL/TLS work with HTTPS?**
   - Understand how SSL/TLS encrypts data between client and server, securing communication by using public and private keys for encryption and authentication.

6. **What is the difference between HTTP/1.1, HTTP/2, and HTTP/3?**
   - HTTP/1.1 is the original version, HTTP/2 introduces multiplexing and header compression, and HTTP/3 uses QUIC, a UDP-based protocol, for faster and more reliable connections.

7. **How do WebSockets differ from HTTP?**
   - Unlike HTTP’s request-response model, WebSockets allow continuous bi-directional communication over a single connection, making them ideal for real-time applications.

8. **What happens when you type a URL into a browser?**
   - This is a broad question that involves DNS resolution, TCP connection setup, HTTP request and response, rendering, and other steps.

9. **What are the limitations of HTTP/1.1, and how does HTTP/2 improve performance?**
   - HTTP/1.1’s sequential request/response system can be slow; HTTP/2 allows multiplexing to send multiple requests over a single connection.
10. **What is gRPC and when should it be used?**
    - gRPC is a high-performance RPC framework that allows for efficient communication between services using HTTP/2. It’s particularly useful in microservices architectures and real-time systems.

## 2. Web Servers

Web servers are responsible for serving web pages to clients. They receive requests from clients (usually browsers) and respond with the requested resources (HTML files, images, etc.). Common web servers include:
- **Apache**: One of the most widely used open-source web servers, known for its flexibility and support for various modules.
- **Nginx**: Known for its high performance and ability to handle a large number of concurrent connections, often used as a reverse proxy and load balancer.
- **Microsoft IIS**: A web server from Microsoft used for hosting websites and web applications on Windows servers, integrating well with ASP.NET.

### Key Topics in Web Servers

#### 1. How Web Servers Work
- **Description**: Web servers process incoming requests from clients, retrieve the necessary resources, and send responses back. This involves interpreting HTTP requests and serving files based on those requests.
- **Key Questions**:
  - What happens during the request-response cycle?
  - How do web servers manage multiple concurrent requests?
  - What is the role of server configuration files (like `.htaccess` for Apache)?

#### 2. Dynamic vs Static Content
- **Description**: Static content is fixed and delivered directly to the client, while dynamic content is generated on-the-fly based on user interaction or server-side processing.
- **Key Questions**:
  - What are examples of static and dynamic content?
  - How do web servers differentiate between static and dynamic content?
  - What technologies are commonly used to serve dynamic content (e.g., PHP, Node.js)?

#### 3. E-Tags
- **Description**: E-Tags (Entity Tags) are used in HTTP responses to provide a unique identifier for a specific version of a resource, helping with cache validation and reducing bandwidth usage.
- **Key Questions**:
  - How do E-Tags improve caching efficiency?
  - What happens if an E-Tag is mismatched during a conditional request?
  - How do E-Tags differ from Last-Modified headers?

#### 4. HTTP Protocol
- **Description**: The Hypertext Transfer Protocol (HTTP) is the foundation for data communication on the web. It defines how messages are formatted and transmitted between clients and servers.
- **Key Questions**:
  - What are the main differences between HTTP/1.1, HTTP/2, and HTTP/3?
  - How do HTTP methods (GET, POST, PUT, DELETE) work?
  - What are the implications of using HTTPS compared to HTTP?



## 3. Database Engineering

Database engineering involves designing, implementing, and managing databases that store, retrieve, and manipulate data efficiently. There are two main types of databases:

- **SQL Databases**: Structured Query Language databases like MySQL, PostgreSQL, and Oracle are based on a relational model, where data is organized in tables with defined relationships.
- **NoSQL Databases**: Non-relational databases like MongoDB and Cassandra handle unstructured or semi-structured data and scale horizontally, allowing for flexible data models and high availability.

### Key Topics in Database Engineering

#### 1. Relational vs NoSQL
- **Description**: Relational databases use a fixed schema and enforce relationships through foreign keys, while NoSQL databases offer flexible schemas and can handle various data types, making them suitable for different use cases.
- **Key Questions**:
  - What are the advantages and disadvantages of relational databases compared to NoSQL databases?
  - In what scenarios would you choose a NoSQL database over a relational database?
  - How do data normalization and denormalization work in relational databases?

#### 2. ACID Properties
- **Description**: ACID (Atomicity, Consistency, Isolation, Durability) properties ensure reliable processing of database transactions, providing a framework for maintaining data integrity.
  - **Atomicity**: Ensures that a transaction is all-or-nothing, meaning if one part of the transaction fails, the entire transaction fails.
  - **Consistency**: Guarantees that a transaction brings the database from one valid state to another, maintaining data integrity.
  - **Isolation**: Ensures that concurrent transactions do not interfere with each other, maintaining the appearance of executing transactions in isolation.
  - **Durability**: Guarantees that once a transaction is committed, it will remain so, even in the event of a system failure.


## 4. Proxies

A proxy server acts as an intermediary between clients and web servers, helping to improve security, performance, and anonymity. There are two main types of proxies:

- **Forward Proxy**: Handles requests from clients seeking resources from servers, acting as a gateway for clients.
- **Reverse Proxy**: Handles requests from external clients on behalf of servers, distributing traffic across multiple servers for load balancing and improved performance.

### Key Topics in Proxies

#### 1. Difference Between Proxy and Reverse Proxy
- **Description**: A forward proxy forwards client requests to the internet, hiding the client's identity, while a reverse proxy forwards requests to one or more servers, hiding the server's identity from clients.
- **Key Questions**:
  - What are the main use cases for forward proxies?
  - In what scenarios is a reverse proxy more beneficial than a forward proxy?
  - How do proxies affect network security and user privacy?

#### 2. Layer 7 Proxy vs Layer 4 Proxy vs Layer 3 Proxy
- **Description**: 
  - **Layer 7 Proxy**: Operates at the application layer (HTTP/HTTPS), allowing for more complex routing based on content and can inspect and modify requests and responses.
  - **Layer 4 Proxy**: Works at the transport layer, forwarding TCP/UDP packets without inspecting the content, suitable for speed and low-latency scenarios.
  - **Layer 3 Proxy**: Operates at the network layer, dealing with IP packets and primarily used for routing.
- **Key Questions**:
  - What are the advantages and disadvantages of using Layer 7 proxies compared to Layer 4 proxies?
  - How does the choice of proxy layer affect performance and resource utilization?
  - In what situations would you choose a Layer 3 proxy over Layer 4 or Layer 7?

#### 3. Reverse Proxy Applications
- **Description**: Reverse proxies can be used for various applications, including load balancing, SSL termination, caching, and serving as an additional layer of security.
- **Key Questions**:
  - How does a reverse proxy enhance the security of web applications?
  - What role do reverse proxies play in microservices architecture?
  - How can reverse proxies improve the performance of static content delivery?

#### 4. Load Balancing Algorithms
- **Description**: Load balancing algorithms distribute client requests across multiple servers to optimize resource use, minimize response time, and avoid overload on any single server. Common algorithms include Round Robin, Least Connections, and IP Hash.



## 5. Caching

Caching improves the performance of web applications by temporarily storing frequently accessed data in fast storage. This reduces the need to fetch data from the primary source repeatedly, leading to faster response times and improved user experience. Common caching mechanisms include:

- **In-Memory Caches**: Tools like Redis and Memcached store data in memory for rapid access, making them ideal for high-performance applications.
- **Browser Caching**: Web browsers cache static resources (like images, CSS) to speed up page load times, reducing server load and bandwidth usage.

### Key Topics in Caching

#### 1. When to Use Caching
- **Description**: Caching should be considered when data is frequently requested, relatively static, or computationally expensive to generate. It is particularly useful for:
  - Improving response times for read-heavy workloads.
  - Reducing latency for repetitive database queries.
  - Enhancing performance for static resources.
- **Key Questions**:
  - What types of data are most suitable for caching?
  - How can caching strategies be optimized for different application scenarios?
  - What are the potential downsides of caching, such as data staleness?

### Message Queue and Pub/Sub

#### 2. When to Use Pub/Sub Messaging vs. Queue
- **Description**: Pub/Sub messaging and queues serve different purposes in message handling:
  - **Pub/Sub**: Best for scenarios where messages need to be distributed to multiple subscribers, such as real-time notifications and event broadcasting.
  - **Message Queues**: Ideal for point-to-point communication where tasks need to be processed sequentially, such as job processing and task scheduling.
- **Key Questions**:
  - In what scenarios would you choose Pub/Sub over traditional queuing systems?
  - How do Pub/Sub systems handle message delivery and acknowledgment?
  - What factors should be considered when designing a messaging architecture?



## 6. API Web Framework

Web frameworks provide tools and libraries to simplify web development. They define the structure of web applications and help developers build features quickly and efficiently. Some popular web frameworks include:


- **Django (Python)**: A high-level web framework that encourages rapid development and clean, pragmatic design. Django includes built-in features for authentication, database management, and URL routing, making it suitable for complex applications.
- **Express (Node.js)**: A minimal and flexible web framework for Node.js that provides a robust set of features for web and mobile applications. It is widely used for building APIs and supports middleware for handling requests and responses.

### Key Topics in API Web Frameworks

#### 1. API Authoring with Frameworks
- **Description**: API authoring involves creating and designing APIs that allow different applications to communicate with each other. Frameworks like Express and Django streamline this process.
- **Key Questions**:
  - How do you design RESTful APIs using Express and Django?
  - What are the best practices for structuring your API endpoints?
  - How do you implement authentication and authorization in your APIs?

#### 2. Framework Comparison
- **Description**: Each framework has its strengths and weaknesses depending on the use case:
  - **Express**: Lightweight and highly customizable, ideal for building microservices and real-time applications.
  - **Django**: Feature-rich and opinionated, best suited for applications that require a full-fledged backend.

- **Key Questions**:
  - When should you choose Flask over Django or Express for API development?
  - What performance considerations should be kept in mind when selecting a framework?
  - How does Rust compare to these frameworks in terms of performance and safety for API development?


## 7. Message Formats

Message formats define the structure of data exchanged between systems, ensuring that both sender and receiver can understand the content. Common message formats include:

- **JSON (JavaScript Object Notation)**: A lightweight, easy-to-read format for structuring data. It is widely used for APIs due to its simplicity and compatibility with most programming languages.
- **XML (eXtensible Markup Language)**: A flexible format used for representing structured data. While less common in modern APIs, it is still used in many legacy systems and applications.
- **Protocol Buffers (protobuf)**: A method developed by Google for serializing structured data. Protobuf is more compact and efficient than JSON or XML, making it suitable for high-performance applications and large-scale data processing.

### Key Topics in Message Formats

#### 1. JSON & Protocol Buffers
- **Description**: Both JSON and Protocol Buffers are popular formats for data interchange, each with its use cases and advantages:
  - **JSON**: Highly human-readable, making it easy to debug and work with. It is often used in web APIs and configurations.
  - **Protocol Buffers**: More efficient in terms of size and speed, especially for large datasets. It requires a predefined schema but allows for backward and forward compatibility.
  
- **Key Questions**:
  - When should you use JSON over Protocol Buffers for API communication?
  - What are the performance trade-offs between using JSON and Protocol Buffers?
  - How do you handle schema evolution with Protocol Buffers?



## 8. Security

Security in web development is crucial to protecting data and systems from malicious attacks. Important security concepts include:

- **SSL/TLS**: Secure Sockets Layer (SSL) and Transport Layer Security (TLS) protocols ensure encrypted communication between clients and servers, preventing eavesdropping and tampering.
- **Encryption**: The process of converting data into a coded format that can only be read by authorized parties. It is essential for protecting sensitive information both in transit and at rest.
- **Firewalls**: Security devices or software that monitor and control incoming and outgoing network traffic based on predetermined security rules. Firewalls act as a barrier between trusted internal networks and untrusted external networks.

### Key Topics in Security

#### 1. TLS, Encryption, and Firewalls
- **Description**: These components work together to provide a secure environment for web applications. TLS encrypts data in transit, while encryption protects data at rest, and firewalls prevent unauthorized access to systems.

- **Key Questions**:
  - How does TLS prevent man-in-the-middle attacks?
  - What are the general best practices for web security?
  - How can you mitigate server denial-of-service (DoS) attacks?
  - What types of server denial-of-service attacks should you be aware of?
  - What is Server Name Indication (SNI) and how does it relate to SSL/TLS?
  - How do you ensure that a database does not leak sensitive information?
  - Which ports should be open on your server for secure operations?
  - Which ports should be closed to enhance security?

