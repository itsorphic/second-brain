# EC2 (Elastic Compute Cloud)

| Type   | Description    |
|--------------- | --------------- |
| On-Demand Instances  | Default Option. Pay by the second while instance is running.   |
| Reserved Instances  | Reserve isntances for 1-3 years (e.g. database server). Savings up to 70%   |
| Spot Instances   | Bid on unused EC2 capacity. Savings up to 90% but can lose instance at any time   |
| Dedicated Hosts   | Book entire physical server and bring own licenses. Can be purchased on-demand or reserved   |
| Dedicated Instances | Ensures no other AWS customer shares your hardware. Pay by the hour. |
| Capacity Reservations | Reserve capacity for instances in a specific availability zone for any duration. |


# Elastic Load Balancing

**Benefits of using EBS**
Managed Service
    - AWS guarantees uptime
    - AWS handles maintenance, upgrades, etc.

Distributes the load across multiple instances, and across availability zones.

Can handle instance failures by doing regular health checks.

Only exposes a single endpoint (DNS) to your application.

**Types of Load Balancers**
| Type | Description |
| -------------- | --------------- |
| Application Load Balancer (ALB) | Handles  HTTP/HTTPS traffic. Layer 7. |
| Network Load Balancer | Handles TCP, UDP, TLS. Ultra-high performance, low latencies. Layer 4 |
| Gateway Load Balancer | Used to deploy and manage third-party virtual appliances such as firewalls, IDS/IPS. |
| Classic Load Balancer | Previous Gen load balancer for use with the EC2-Classic network |


# Auto Scaling Groups (ASG)

Automatically scale out/in instances based on the load.
    - Specify instance numbers: desired capacity, minimum and maximum.
    - Registers new instances with the load balancer.

Replace unhealthy instances automatically.

Run at optimal capacity, meaning cost savings.





































































