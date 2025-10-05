## Easy Questions

1. What is AWS Route 53?  
   - A scalable and highly available DNS, domain registration, and health-checking service.

2. What is DNS?  
   - Domain Name System translates human-readable domain names to IP addresses.

3. What is a domain name?  
   - A human-readable address used to access websites, like example.com.

4. What is a hosted zone in Route 53?  
   - A container that holds DNS records for a domain.

5. Name two types of hosted zones.  
   - Public hosted zone and private hosted zone.

6. What is an A record?  
   - Maps a domain to an IPv4 address.

7. What is a CNAME record?  
   - Points an alias domain or subdomain to a canonical domain.

8. What is an MX record used for?  
   - Directs email traffic to a domain's mail server.

9. What is an NS record?  
   - Specifies the authoritative name servers for a domain.

10. Can Route 53 perform health checks?  
    - Yes, it monitors resources and routes traffic to healthy endpoints.

## Moderate Questions

1. What is the difference between public and private hosted zones?  
   - Public hosted zones route traffic from the internet; private hosted zones route traffic within a VPC.

2. How does DNS resolver work when a domain is requested?  
   - It queries root, TLD, and authoritative servers to find the domain’s IP address.

3. What is a subdomain?  
   - An optional prefix added to a domain to organize website sections, e.g., blog.example.com.

4. What is geolocation routing in Route 53?  
   - Routes traffic based on the geographic location of the user.

5. What is latency routing policy?  
   - Routes traffic to the AWS region with the lowest latency for the user.

6. Explain failover routing policy.  
   - Routes traffic to a secondary resource if the primary fails.

7. What is multivalue answer routing policy?  
   - Returns multiple healthy records in response to DNS queries.

8. What is weighted routing policy?  
   - Routes traffic to multiple resources based on assigned weights.

9. What is geoproximity routing?  
   - Routes traffic based on resource locations and optional traffic shifting.

10. How can Route 53 integrate with AWS resources like S3 or EC2?  
    - By pointing DNS records to the respective resource endpoints.

## Hard Questions

1. Describe the full DNS resolution process in Route 53.  
   - User request → DNS resolver → cache → root server → TLD → authoritative server → IP returned.

2. How does Route 53 support high availability?  
   - By distributing DNS resolution globally with multiple redundant endpoints.

3. Can Route 53 route traffic to non-AWS resources?  
   - Yes, using public hosted zones and proper DNS records.

4. How does Route 53 handle failover for multiple regions?  
   - Using failover or latency routing to route users to healthy endpoints.

5. How do you secure a private hosted zone?  
   - By associating it with specific VPCs and restricting access via security groups.

6. Explain the difference between geolocation and geoproximity routing.  
   - Geolocation is based on user location; geoproximity is based on resource location with optional traffic shifting.

7. How do weighted and multivalue routing differ?  
   - Weighted routing distributes traffic based on percentage; multivalue routing returns multiple healthy records randomly.

8. Can Route 53 perform DNS failover for email servers?  
   - Yes, MX records with health checks can be used for failover.

9. How does Route 53 integrate with CloudFront for global content delivery?  
   - By pointing DNS records to CloudFront distributions as origins.

10. How does TTL affect DNS caching in Route 53?  
    - It defines how long a DNS resolver caches the record before querying Route 53 again.
