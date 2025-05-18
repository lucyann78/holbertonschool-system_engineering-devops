Simple Web Stack

![image alt](https://github.com/lucyann78/holbertonschool-system_engineering-devops/blob/bd83c4fb49d11f5afd81820817f1bc25dc528c7c/Web%20Infrastructures%20Mermaid%20Diagram.png)
Component in the Diagram
User:

The individual trying to access the website www.foobar.com. This initiates the request to the web infrastructure.
DNS (Domain Name System):

Resolves the domain name www.foobar.com to the server's IP address (8.8.8.8). It acts as a phone book for the internet, translating user-friendly domain names into machine-readable IP addresses.
Server IP (8.8.8.8):

The address of the server hosting the web application. This is where all requests from users are directed after DNS resolution.
Nginx Web Server:

Handles incoming HTTP/HTTPS requests from users. It serves static content (like HTML, CSS, and JavaScript files) and acts as a reverse proxy to forward requests to the application server for dynamic content.
Application Server:

Executes the application logic. It processes requests that require database interactions or other backend services. It retrieves data from the database and sends it back to the web server, which then serves it to the user.
MySQL Database:

Stores data for the application, such as user information, posts, or other relevant content. It allows the application server to perform CRUD (Create, Read, Update, Delete) operations on the data.
Application Code Base:

Contains the source code for the application. This is where the business logic resides, and it is executed by the application server to generate dynamic responses for users.
System Redundancy
System Redundancy: This refers to the inclusion of extra components that are not strictly necessary for functionality but serve as backups to ensure system reliability and availability. In the context of web infrastructure:
Redundant Servers: Multiple servers can be set up to handle user requests. If one server fails, others can take over, preventing downtime.
Load Balancers: Distribute incoming traffic across multiple servers, ensuring no single server becomes a bottleneck, improving performance and fault tolerance.
Acronyms Explained
LAMP:

Stands for Linux, Apache, MySQL, and PHP. It is a popular stack for web development, providing an open-source platform for building dynamic websites and applications.
SPOF (Single Point of Failure):

A component in a system whose failure would lead to the entire system failing. In the context of the initial infrastructure, if the single server goes down, the entire website becomes unavailable.
QPS (Queries Per Second):

A measure of how many database queries are processed by the server each second. It is an important metric for assessing the performance and scalability of a web application.
