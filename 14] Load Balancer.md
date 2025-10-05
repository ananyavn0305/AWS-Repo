## Easy Level

1. **What is an Elastic Load Balancer (ELB)?**  
   A service that automatically distributes incoming application traffic across multiple targets/servers.

2. **Primary role of a Load Balancer?**  
   Evenly distribute incoming traffic to prevent any single server from becoming overwhelmed.

3. **What is a Target Group?**  
   A set of resources that a load balancer routes traffic to.

4. **What protocols does Application Load Balancer (ALB) support?**  
   HTTP and HTTPS.

5. **At which OSI layer does ALB operate?**  
   Layer 7 (Application Layer).

6. **At which OSI layer does Network Load Balancer (NLB) operate?**  
   Layer 4 (Transport Layer).

7. **Protocols supported by NLB?**  
   TCP and UDP.

8. **What is Gateway Load Balancer?**  
   Load balancer for deploying, scaling, and managing third-party virtual appliances (firewalls, IDS/IPS).

9. **AWS Global Accelerator purpose?**  
   Improves availability and performance by routing traffic through AWS global network instead of public internet.

10. **Does ELB perform health checks?**  
    Yes, regularly checks target health and stops sending traffic to unhealthy servers.

## Moderate Level

11. **Scenario: Your app experiences uneven traffic across servers. Solution?**  
    Use an ELB to distribute traffic evenly.

12. **Scenario: Need to route traffic based on URL or path. Which ELB type?**  
    Application Load Balancer (ALB).

13. **Scenario: Need to handle millions of TCP connections with low latency. Which ELB type?**  
    Network Load Balancer (NLB).

14. **Scenario: Deploy a firewall appliance for all traffic in VPC. Which ELB type?**  
    Gateway Load Balancer.

15. **Scenario: Want static IPs for a globally distributed application. Solution?**  
    Use AWS Global Accelerator.

16. **Scenario: One server becomes unhealthy. What happens?**  
    ELB stops sending traffic to it until it is healthy again.

17. **Scenario: Need automatic failover if one AWS region goes down. Solution?**  
    AWS Global Accelerator routes traffic to another healthy region.

18. **Scenario: Optimize latency for users connecting from multiple countries. Solution?**  
    AWS Global Accelerator directs traffic via the fastest path.

19. **Scenario: Dynamically scale servers behind load balancer. How?**  
    Add/remove servers in the target group; ELB handles traffic distribution automatically.

20. **Scenario: Need HTTPS termination for multiple web apps. Which ELB?**  
    ALB can terminate SSL/TLS and route traffic based on host/path.

## Hard Level / Scenario-Based

21. **Scenario: High-throughput TCP application requires Layer 4 load balancing. Which ELB?**  
    Network Load Balancer (NLB).

22. **Scenario: Deploy third-party firewall appliances that must scale automatically. Solution?**  
    Gateway Load Balancer.

23. **Scenario: Users report slow response times from your app. How can Global Accelerator help?**  
    Routes traffic through AWS global network to minimize latency.

24. **Scenario: Your web app needs to route requests differently based on URL paths. Which ELB?**  
    ALB, because it operates at Layer 7 and supports path-based routing.

25. **Scenario: You need to maintain sticky sessions for users. Which ELB?**  
    ALB supports sticky sessions (session affinity).

26. **Scenario: One region fails, users are rerouted automatically. How?**  
    AWS Global Accelerator detects unhealthy endpoints and shifts traffic.

27. **Scenario: Need TCP and UDP support with static IPs. Which combination?**  
    Use NLB for Layer 4 traffic and AWS Global Accelerator for static IP routing.

28. **Scenario: Elasticity required for backend servers. How ELB helps?**  
    Add/remove servers in target groups; ELB balances traffic dynamically.

29. **Scenario: Monitor target health and avoid routing to failed servers. How?**  
    Configure health checks in ELB; unhealthy targets are removed automatically.

30. **Scenario: High volume of web requests from different regions. Ensure low latency. Solution?**  
    Use ALB or NLB with AWS Global Accelerator to optimize traffic routing.

31. **Scenario: Secure traffic termination at load balancer. How?**  
    ALB or NLB with TLS/SSL certificates handles HTTPS termination.

32. **Scenario: Multi-tier architecture with multiple services. How ELB helps?**  
    Create multiple target groups for each service and route traffic accordingly.

33. **Scenario: Application requires failover across AZs. How?**  
    ELB automatically distributes traffic across multiple Availability Zones.

34. **Scenario: Reduce impact of sudden spikes in traffic. How ELB helps?**  
    ELB distributes load and works with Auto Scaling to add instances dynamically.

35. **Scenario: Want to route traffic to specific EC2 instances based on IP or port. Solution?**  
    NLB can route based on TCP/UDP ports.

36. **Scenario: Multiple microservices deployed in containers. How to load balance?**  
    ALB supports path-based routing to route to different microservices.

37. **Scenario: Need to inspect traffic with firewall appliances transparently. How?**  
    Gateway Load Balancer with third-party appliances.

38. **Scenario: Need persistent connections for backend TCP servers. Which ELB?**  
    NLB, because it supports TCP with high throughput and low latency.

39. **Scenario: Reduce internet latency for global users without changing app code. Solution?**  
    AWS Global Accelerator with static IPs.

40. **Scenario: Health checks failing for backend servers. How to troubleshoot?**  
    Check target health, security groups, and instance configuration.

41. **Scenario: Multiple target groups per load balancer. Purpose?**  
    Route different types of traffic to different sets of servers (e.g., microservices).

42. **Scenario: ELB not distributing traffic evenly. What to check?**  
    Check target group registration, health status, and load balancer configuration.

43. **Scenario: Need to connect on-premises users to AWS app via optimized route. Solution?**  
    AWS Global Accelerator ensures fast, reliable routing.

44. **Scenario: Want to scale backend servers automatically during traffic spikes. Solution?**  
    ELB with Auto Scaling adjusts target group dynamically.

45. **Scenario: High availability requirement across AZs. How ELB ensures this?**  
    Distributes traffic across multiple Availability Zones for fault tolerance.

46. **Scenario: Global app requires routing to nearest healthy region. How?**  
    AWS Global Accelerator automatically detects and routes to nearest healthy region.

47. **Scenario: Need both HTTP and TCP load balancing. How?**  
    Use ALB for HTTP/HTTPS and NLB for TCP/UDP traffic.

48. **Scenario: Want load balancer to detect unhealthy EC2s and reroute traffic. How?**  
    Configure health checks; ELB stops sending requests to unhealthy targets.

49. **Scenario: Reduce impact of backend failures during updates. How?**  
    ELB with health checks and multiple AZ deployment ensures smooth traffic distribution.

50. **Scenario: Application needs SSL offloading. Which ELB type?**  
    ALB or NLB with TLS termination.
