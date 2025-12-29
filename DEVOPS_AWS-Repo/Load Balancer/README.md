🌐 AWS Load Balancer – Brief & Easy Notes
4
What is Elastic Load Balancing (ELB)?

AWS Load Balancer automatically distributes incoming traffic across multiple servers (EC2, containers, IPs) to ensure:

High availability

Better performance

Fault tolerance

👉 Simple meaning:
It prevents one server from getting overloaded.

🔹 Types of AWS Load Balancers
1️⃣ Application Load Balancer (ALB)

Works at Layer 7 (HTTP/HTTPS)

Used for web applications

✔ Path-based routing (/login, /api)
✔ Host-based routing
✔ Supports containers & microservices

📌 Best for: Web apps, APIs

2️⃣ Network Load Balancer (NLB)

Works at Layer 4 (TCP/UDP)

Handles very high traffic

Extremely low latency

✔ Static IP support
✔ Millions of requests/sec

📌 Best for: Real-time apps, gaming, VoIP

3️⃣ Gateway Load Balancer (GWLB)

Used for security appliances

Traffic inspection (firewalls, IDS/IPS)

📌 Best for: Network security solutions

4️⃣ Classic Load Balancer (CLB) (Legacy)

Layer 4 & Layer 7

Not recommended for new apps

🔹 Core Components of Load Balancer
🔸 Listener

Checks port & protocol

Example: HTTP 80, HTTPS 443

🔸 Target Group

Group of backend servers

Targets:

Amazon EC2

IP addresses

Containers

🔸 Health Checks

Checks server health

Sends traffic only to healthy targets

🔹 How Load Balancer Works (Simple Flow)

User sends request

Load Balancer receives traffic

Health check verifies targets

Traffic forwarded to healthy server

Response sent back to user

🔹 High Availability & Fault Tolerance

Load balancers work across multiple Availability Zones

Automatically reroutes traffic if one AZ fails

🔹 Security Features

Works with Security Groups

SSL/TLS termination

Integrates with AWS Certificate Manager

Supports AWS WAF

🔹 Load Balancer Algorithms

Round Robin (default)

Least outstanding requests (ALB)

Flow hash (NLB)

🔹 Pricing (Simple)

You pay for:

Load balancer hours

Data processed (LCU / NLCU)

💡 No upfront cost

✅ Benefits of AWS Load Balancer

Improves availability

Automatic scaling

Handles traffic spikes

Secure & reliable

Easy integration with Auto Scaling

❌ Limitations

Additional cost

Misconfiguration can cause latency

Classic LB is outdated

🔹 Load Balancer vs Auto Scaling
Feature	Load Balancer	Auto Scaling
Traffic distribution	✅	❌
Scale instances	❌	✅
Fault tolerance	✅	✅

👉 Both are used together in production.
