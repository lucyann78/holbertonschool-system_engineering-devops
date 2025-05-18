# Project Overview

This project aims to design and implement various web infrastructures, enhancing your understanding of web stack components, their interactions, and the importance of redundancy and security in web architecture. By the end of this project, you will be able to explain each component of the web stack and its role in delivering web services effectively.

Learning Objectives
Diagram Creation: You will learn to draw a diagram of the web stack you built, demonstrating your understanding of how different components interact.
Component Explanation: You will be able to explain the function of each component within the web infrastructure.
System Redundancy: You will understand the concept of redundancy and its importance in maintaining system availability and reliability.
Acronyms: Familiarity with key acronyms such as LAMP, SPOF, and QPS will be developed.
Requirements
A README.md file must be present at the root of the project folder.
For each task, create a diagram and take a screenshot of your work.
Upload screenshots to an image hosting service and include the links in your answer file.
Push your answer file to GitHub and provide the repository link.
Each task must be whiteboarded in front of a mentor or peer without notes.
Focus on the requirements; detailed explanations are not necessary unless requested.
Tasks
Task 0: Simple Web Stack
Purpose: Design a one-server web infrastructure to host the website accessible via www.foobar.com. This task emphasizes understanding the basic components of a web stack.
Components:
Domain name: Configured with a www record pointing to the server IP (8.8.8.8).
Server: Includes a web server (Nginx), application server, application files, and a MySQL database.
Key Concepts: Understand the roles of the domain name, web server, application server, and database, as well as issues like SPOF and downtime.
Task 1: Distributed Web Infrastructure
Purpose: Create a three-server web infrastructure to enhance scalability and load management for www.foobar.com.
Components:
Load balancer (HAproxy) and two servers, each with a web server, application server, and database.
Key Concepts: Explain the distribution algorithm for the load balancer, the differences between Active-Active and Active-Passive setups, and how a Primary-Replica database cluster functions.
Task 2: Secured and Monitored Web Infrastructure
Purpose: Design a secure and monitored three-server web infrastructure for www.foobar.com to ensure data integrity and performance tracking.
Components:
Three firewalls, an SSL certificate for HTTPS, and three monitoring clients.
Key Concepts: Explain the purpose of firewalls, the importance of HTTPS traffic, and how monitoring tools collect data, including QPS monitoring.
Task 3: Scale Up
Purpose: Expand the infrastructure by adding a server and configuring load balancers in a cluster to improve performance and reliability.
Components:
One additional server and a load balancer (HAproxy), with separated components for web, application, and database servers.
Key Concepts: Discuss the reasons for adding each component and the benefits of splitting services across servers.
