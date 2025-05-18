# Scale up



## Diagram Components

### 1. HAProxy Load Balancers (LB₁ & LB₂)
Description: Two instances of HAProxy configured as load balancers.
Functionality:
High Availability: Both load balancers share a floating Virtual IP (VIP) managed by Keepalived, ensuring that if one load balancer fails, the other can seamlessly take over without downtime.
Traffic Distribution: Distributes incoming client requests across multiple web servers to optimize resource use and enhance performance.

### 2. Web Server
Description: A dedicated server that handles incoming web traffic.
Functionality:
TLS Termination: Manages the decryption of HTTPS traffic, allowing secure connections while offloading this resource-intensive process from application servers.
Security: Ensures that all incoming traffic is encrypted, protecting sensitive data from interception.

### 3. Nginx
Description: A high-performance web server and reverse proxy server.
Functionality:
Static File Management: Serves static content (like images, CSS, and JavaScript files) directly to clients, reducing the load on application servers.
Caching: Implements caching mechanisms to store frequently accessed content, improving response times for users.
Dynamic Request Proxying: Forwards requests for dynamic content to the application server, acting as an intermediary.

### 4. Application Server
Description: The server that runs the application logic.
Functionality:
Backend Processing: Handles business logic, user authentication, and data processing tasks.
Database Queries: Interacts with the database to retrieve and manipulate data as needed, ensuring efficient resource management by separating concerns.

### 5. Database Server
Description: A dedicated server running MySQL.
Functionality:
Data Centralization: Stores all application data in a single location, ensuring data consistency and integrity.
I/O Optimization: Configured for optimal input/output operations and storage management, allowing for efficient data retrieval and storage.

### 6. Monitoring Agents
Description: Software agents installed on each node (load balancers, web servers, application servers, and database servers).
Functionality:
Data Collection: Gathers logs, metrics, and traces from each component, providing insights into system performance and health.
Alerting: Pushes collected data to a monitoring SaaS (Software as a Service) for analysis, enabling proactive identification of potential issues.

