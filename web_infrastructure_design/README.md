# Web Infrastructure Project
## Simple Web Stack
This task involves designing a basic web infrastructure using a single server with a LAMP stack to host the website www.foobar.com. The setup includes a web server (Nginx), an application server, application files, and a MySQL database. Key components are explained, highlighting their roles and the potential issues such as single points of failure and downtimes during maintenance.

## Distributed Web Infrastructure
In this task, the infrastructure is expanded to a three-server setup that includes a load balancer (HAProxy) and two servers, each with a web server, application server, and MySQL database. The load balancer distributes incoming traffic, improving reliability and performance. This design addresses issues like single points of failure and scalability, while also explaining the distribution algorithms used and the differences between Active-Active and Active-Passive setups.

## Secured and Monitored Web Infrastructure
This task enhances the previous design by adding security and monitoring features. The infrastructure now includes three firewalls, an SSL certificate for HTTPS traffic, and three monitoring clients. Each component is justified, focusing on the importance of secure traffic and continuous monitoring. Issues such as SSL termination at the load balancer level and having a single writable MySQL server are discussed, emphasizing the need for robust security measures.

## Scale Up
The final task involves scaling the infrastructure further by introducing an additional server and configuring the load balancer in a cluster setup. Each component—web server, application server, and database—is split across separate servers to optimize performance and manageability. The rationale behind this architecture is explained, focusing on the benefits of distributed components in handling increased traffic and improving overall system resilience.

