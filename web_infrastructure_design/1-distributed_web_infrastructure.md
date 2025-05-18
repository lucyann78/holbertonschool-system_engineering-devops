# Distributed Web Infrastructure

![image alt](https://github.com/lucyann78/holbertonschool-system_engineering-devops/blob/3329155a7de055cb37627e680640f5ba561a0276/web_infrastructure_design/Distributed%20Web%20Infrastructure%20Mermaid%20Diagram.png)

This architecture diagram illustrates a typical web application deployment with load balancing, application servers, a MySQL database cluster, and highlights potential vulnerabilities and areas for improvement. Understanding each component's role helps in optimizing performance, enhancing security, and ensuring the reliability of the overall system.

## 1. Client Requests
Description: Represents users or clients accessing the web application from various devices (e.g., desktops, smartphones).
Function: Initiates requests to the web application, such as loading a webpage or submitting a form.
## 2. Load Balancer (HAProxy)
Description: A software-based load balancer that distributes incoming traffic across multiple servers.
Function:
Traffic Distribution: Ensures that no single server is overloaded by evenly distributing client requests.
Health Checks: Monitors the health of backend servers and directs traffic only to those that are operational.
Session Persistence: Can maintain user sessions by directing requests from the same client to the same server if needed.
Configuration Options
Load Balancing Algorithms: Can use methods like round-robin, least connections, or IP hash to determine how to distribute requests.
Active-Active vs. Active-Passive
Active-Active: All servers are actively processing requests, leading to better resource utilization.
Active-Passive: One server is active while others are on standby, which may lead to underutilization.
## 3. Server 1 and Server 2
Description: Two identical servers that host the web application components.
Function: Each server handles a portion of the incoming requests, providing redundancy and load distribution.
### Components of Each Server:
Web Server (Nginx)

Description: A high-performance web server that serves static content and forwards dynamic requests to the application server.
Function:
Static Content Delivery: Serves files like HTML, CSS, and JavaScript efficiently.
Reverse Proxy: Forwards requests for dynamic content to the application server.
### Application Server

Description: Executes the application logic and processes requests from the web server.
Function:
Business Logic Processing: Handles the application's core functionalities, such as user authentication and data processing.
Communication with Database: Interacts with the database to read/write data as required.
### Set of Application Files

Description: Contains the source code and resources needed for the application to function.
Function: Supports the application server in delivering dynamic content and functionalities.
### Database (MySQL)

Description: A relational database management system that stores application data.
Function:
Data Storage: Permanently stores user data, application state, and other critical information.
Primary-Replica (Master-Slave) Configuration:
Primary Node: Handles all write operations and serves as the main data source.
Replica Node: Receives updates from the primary node and handles read operations, improving performance and redundancy.
### Differences Between Primary and Replica Nodes
Primary Node: Responsible for processing all write requests and maintaining the authoritative version of the data.
Replica Node: Used primarily for read operations, reducing the load on the primary node and providing failover capabilities.

