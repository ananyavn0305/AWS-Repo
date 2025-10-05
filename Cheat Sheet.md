## **AWS Introduction & Core Concepts**
- **AWS:** Cloud platform offering computing, storage, databases, networking, and other services.  
- **Cloud Models:** IaaS (EC2, VPC), PaaS (Elastic Beanstalk), SaaS (WorkDocs).  
- **Regions & AZs:** Regions are geographic areas; AZs are isolated data centers within regions.  
- **Edge Locations:** Serve content via CloudFront for low latency.  

---

## **EC2 & IAM**
- **EC2:** Virtual servers; choose AMI, instance type, storage, security.  
- **Elastic IP:** Static IP for EC2.  
- **Security Groups:** Firewall for instances.  
- **Key Pairs:** For SSH authentication.  
- **IAM:** Manage users, roles, and permissions.  

---

## **S3 & EBS**
- **S3:** Object storage; buckets, objects, keys, versioning, storage classes (Standard, IA, Glacier).  
- **EBS:** Block-level storage for EC2; persistent; snapshots for backup.  

---

## **VPC**
- **VPC:** Isolated network for AWS resources.  
- **Subnets:** Public/private; control traffic flow.  
- **Components:** Internet Gateway, NAT Gateway, Route Tables, Security Groups, NACLs.  

---

## **VPC Peering & Networking**
- **VPC Peering:** Connects VPCs privately; no transitive routing.  
- **Direct Connect:** Dedicated on-premises to AWS connection.  
- **VPC Endpoints:** Private access to AWS services (Interface/Gateway).  
- **Placement Groups:** Cluster, Spread, Partition for EC2 placement.  
- **NIC:** Virtual network interface attached to EC2.  

---

## **EFS**
- **Elastic File System:** Scalable file storage, accessed by multiple EC2s.  
- **Storage Classes:** Standard & Infrequent Access.  
- **Protocol:** NFS.  
- **EBS vs EFS:** EFS → multi-instance, auto-scalable; EBS → single instance, fixed size.  

---

## **Load Balancers**
- **ELB:** Distributes incoming traffic across targets.  
- **ALB:** Layer 7, HTTP/HTTPS.  
- **NLB:** Layer 4, TCP/UDP, high throughput.  
- **Gateway LB:** Layer 3/4, deploy virtual appliances.  
- **Global Accelerator:** Optimizes global application performance and availability.  

---

## **Autoscaling**
- **Autoscaling:** Automatically adjusts resources based on demand.  
- **Horizontal Scaling:** Add more instances.  
- **Vertical Scaling:** Increase instance capacity.  
- **Manual vs Dynamic:** Manual → user-defined; Dynamic → automatic based on traffic.  

---

## **RDS**
- **RDS:** Managed relational databases (MySQL, PostgreSQL, Aurora, Oracle, SQL Server).  
- **DB Concepts:** Database, DBMS, Relational vs Non-relational.  
- **Connect RDS to EC2:** Configure security groups, install DB client, connect via endpoint, execute SQL queries.  

---

## **CloudWatch**
- **CloudWatch:** Monitors AWS resources & apps; metrics, logs, events.  
- **Alarms:** Trigger actions (OK, ALARM, INSUFFICIENT_DATA).  
- **Logs:** Centralized log storage.  
- **Events:** Near real-time operational events.  
- **SNS:** Notifications from CloudWatch (pub-sub model).  

---

## **AWS CLI**
- **AWS CLI:** Command-line tool to manage AWS.  
- **Common Commands:**  
  - `aws configure` → credentials setup.  
  - `aws ec2 run-instances` → launch EC2.  
  - `aws s3api create-bucket` → create S3 bucket.  
  - Key pair creation & SSH access.  

---

## **CloudFront**
- **CloudFront:** CDN for fast, low-latency content delivery.  
- **Edge Locations:** Deliver cached content near users.  
- **Distributions:** Rules defining content delivery from origin to edge.  

---

## **Route 53**
- **Route 53:** DNS, domain registration, health checks.  
- **DNS:** Translates domain names to IP addresses.  
- **Components:** Domain, SLD, TLD, Subdomain.  
- **Hosted Zones:** Public (internet) & Private (within VPC).  
- **Records:** A, AAAA, CNAME, NS, MX.  
- **Routing Policies:** Simple, Failover, Geolocation, Geoproximity, Latency, Weighted, Multivalue Answer.  
