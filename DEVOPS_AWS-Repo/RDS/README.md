🌩️ Amazon RDS (Relational Database Service) – Complete & Easy Explanation
4
What is Amazon RDS?

Amazon RDS is a fully managed database service provided by Amazon Web Services that makes it easy to set up, operate, and scale relational databases in the cloud.

👉 In simple words:
You focus on using the database, AWS handles installation, backups, patching, security, and scaling.

🔹 Databases Supported by Amazon RDS

Amazon RDS supports popular relational databases:

Database Engine	Description
MySQL	Popular open-source DB for web apps
PostgreSQL	Advanced open-source DB
MariaDB	MySQL-compatible DB
Oracle Database	Enterprise-grade DB
Microsoft SQL Server	Microsoft ecosystem DB
Amazon Aurora	AWS high-performance DB (MySQL & PostgreSQL compatible)
🔹 How Amazon RDS Works (Simple Flow)

You create a DB instance

Choose:

Database engine (MySQL, PostgreSQL, etc.)

Instance size (CPU, RAM)

Storage type

AWS automatically:

Installs DB software

Manages OS & DB patches

Takes backups

Monitors health

You connect your application using:

Endpoint

Username & Password

🔹 Key Components of RDS
1️⃣ DB Instance

A running database server

Has CPU, RAM, storage, and endpoint

2️⃣ Storage

General Purpose (gp3/gp2) – normal workloads

Provisioned IOPS (io1/io2) – high performance DBs

3️⃣ Endpoint

DNS name used by applications to connect
(Example: mydb.xxxxxx.ap-south-1.rds.amazonaws.com)

🔹 High Availability – Multi-AZ
What is Multi-AZ?

Primary DB in one Availability Zone

Standby DB in another AZ

Automatic failover if primary fails

✅ Benefits

High availability

Disaster recovery

No manual intervention

🔹 Read Replicas (For Performance)
What are Read Replicas?

Copies of your main database

Used for read-heavy workloads

📌 Example:

Main DB → Writes

Read Replica → Reports, analytics

🔹 Backup & Recovery
Automated Backups

Enabled by default

Retention: 1–35 days

Point-in-Time Recovery

Manual Snapshots

User-initiated

Stored until deleted

Useful before upgrades

🔹 Security in Amazon RDS
🔐 Network Security

Runs inside Amazon VPC

Controlled using Security Groups

🔐 Encryption

At Rest → AWS KMS

In Transit → SSL/TLS

🔐 Authentication

DB username/password

IAM Authentication (for MySQL & PostgreSQL)

🔹 Monitoring & Performance
Tools Used

Amazon CloudWatch

Performance Insights

Enhanced Monitoring

You can track:

CPU usage

Memory

Disk I/O

Connections

🔹 Scaling in RDS
Vertical Scaling

Increase instance size (CPU/RAM)

Storage Scaling

Increase storage without downtime (most cases)

Read Scaling

Add Read Replicas

🔹 Pricing Model (Pay As You Go)

You pay for:

DB instance hours

Storage used

I/O operations

Backup storage (beyond free limit)

Data transfer

💡 No upfront cost (unless Reserved Instances)

✅ Benefits of Amazon RDS
🌟 Major Advantages

No server management

Automatic backups

High availability (Multi-AZ)

Easy scaling

Strong security

Monitoring & alerts

Cost-effective for production workloads

❌ Limitations of RDS

Limited OS-level access (no root)

Not ideal for non-relational data

Some advanced DB features may be restricted

🔹 RDS vs EC2 Database (Quick Comparison)
Feature	RDS	EC2
Setup	Easy	Manual
Backup	Automatic	Manual
Scaling	Simple	Complex
Maintenance	AWS	You
Root Access	❌	✅
🧠 When Should You Use Amazon RDS?

✔ Web applications
✔ Enterprise applications
✔ ERP / CRM systems
✔ Production databases
✔ When you want less operational overhead
