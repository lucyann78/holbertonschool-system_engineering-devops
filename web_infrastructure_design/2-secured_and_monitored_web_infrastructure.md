# Secure and Monitored Web Infrastructure

![image alt](https://github.com/lucyann78/holbertonschool-system_engineering-devops/blob/98fe2fd33402157a75e893bf90c3f6c3ed3e0e96/web_infrastructure_design/Secure%20and%20Monitor%20Web%20InfrastructureMermaid%20diagram.png)

## Diagram Components

### Firewalls:

Edge Firewall: Protects against external threats.
Internal Firewall: Segments the network, ensuring secure communication between the load balancer, application servers, and database.
### SSL/TLS Certificate:

Deployed on the load balancer and application servers to encrypt traffic, ensuring data security and authenticity.
### Monitoring Agents:

Three agents installed on servers to collect logs, metrics, and traces, sending this data to a SaaS for analysis and alerting.
### MySQL Cluster:

Primary: Handles write operations.
Replica: Provides redundancy and handles read queries.
#### Remaining Issues & Next Steps
SSL Termination: Consider end-to-end TLS to secure traffic between the load balancer and backend servers.
Single MySQL Write Primary: Implement automatic failover or multi-primary clustering to enhance availability.
Server Role Separation: Isolate roles onto dedicated servers or containers for improved security and manageability.
