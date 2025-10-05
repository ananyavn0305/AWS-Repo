## Easy Level

1. **What is VPC Peering?**  
   A networking connection between two or more VPCs allowing them to communicate as if in the same network.

2. **Can VPC peering connect VPCs in different regions?**  
   Yes, inter-region VPC peering is supported.

3. **Does VPC peering support transitive routing?**  
   No, traffic cannot be routed through a peered VPC to reach another VPC.

4. **What is AWS Direct Connect?**  
   Dedicated connection from on-premises network to one or more VPCs.

5. **What is a VPC Endpoint?**  
   Allows private, secure access to AWS services from a VPC without an Internet Gateway or NAT.

6. **Types of VPC Endpoints?**  
   Interface Endpoints and Gateway Endpoints.

7. **What is an Interface Endpoint?**  
   Uses AWS PrivateLink to connect to AWS services privately via a network interface.

8. **What is a Gateway Endpoint?**  
   A virtual device that adds a route to your VPC route tables to connect to AWS services.

9. **What is a Placement Group?**  
   Logical grouping of EC2 instances to control how they are placed on underlying hardware.

10. **Types of Placement Groups?**  
    Cluster, Spread, and Partition.
    
## Moderate Level

11. **Scenario: You want EC2 instances in the same AZ to have low-latency connectivity. Which placement group?**  
    Cluster placement group.

12. **Scenario: You want to reduce risk of correlated hardware failures. Which placement group?**  
    Spread or Partition placement group.

13. **Scenario: You want to group instances across multiple partitions in one AZ. Which strategy?**  
    Partition placement group.

14. **What is NIC in VPC context?**  
    Network Interface (Elastic Network Interface) attached to an EC2 instance.

15. **Scenario: Need private access to S3 from VPC without internet. Solution?**  
    Use Gateway VPC Endpoint for S3.

16. **Scenario: Connect EC2 instances in VPC A to RDS in VPC B. How?**  
    Create VPC Peering between VPC A and B, update route tables.

17. **Scenario: Multiple VPCs need to communicate without internet. How?**  
    Direct VPC Peering between each pair.

18. **Scenario: Want dedicated connection from on-premises to VPC for low latency. Solution?**  
    AWS Direct Connect.

19. **Scenario: VPC Peering not working across regions. What to check?**  
    Ensure inter-region VPC peering enabled, route tables updated, no overlapping CIDRs.

20. **Scenario: EC2 cannot reach service via Interface Endpoint. What to check?**  
    Security groups, NACLs, endpoint DNS name, private link configuration.

21. **Scenario: Minimize risk of instance failure in same rack. Placement strategy?**  
    Spread placement group.

22. **Scenario: Minimize impact of correlated hardware failures across partitions. Placement strategy?**  
    Partition placement group.

23. **Scenario: Want high-bandwidth connectivity for tightly coupled instances. Placement strategy?**  
    Cluster placement group.

24. **Scenario: Attach multiple NICs to single EC2 instance. Why?**  
    To connect to multiple subnets, segregate traffic, or assign multiple IPs.

25. **Scenario: Interface endpoint vs Gateway endpoint. Difference?**  
    Interface: uses network interface, PrivateLink.  
    Gateway: virtual device, route to service (S3, DynamoDB).

26. **Scenario: EC2 in VPC A cannot ping EC2 in VPC B after peering. What to check?**  
    Route tables, security groups, NACLs, DNS settings.

27. **Scenario: Peering VPCs with overlapping CIDRs. Solution?**  
    Cannot create VPC peering; must choose non-overlapping CIDRs.

28. **Scenario: Allow S3 access in private subnet without NAT. Solution?**  
    Use Gateway Endpoint.

29. **Scenario: High-performance computing cluster in single AZ. Placement strategy?**  
    Cluster placement group for low-latency, high-bandwidth networking.

30. **Scenario: Secure access to AWS service from VPC without internet. Option?**  
    Interface Endpoint or Gateway Endpoint depending on service.

## Hard Level / Scenario-Based

31. **Scenario: You need EC2 in VPC A to access multiple VPCs. Solution?**  
    Create direct peering with each VPC; transitive routing not allowed.

32. **Scenario: Need to connect on-premises network to multiple VPCs efficiently. Solution?**  
    Use AWS Direct Connect + Transit Gateway.

33. **Scenario: Want EC2 instances to communicate across accounts privately. Solution?**  
    VPC Peering across accounts with route tables updated.

34. **Scenario: Need to mount multiple ENIs to instance for traffic isolation. How?**  
    Attach multiple NICs with separate security groups and IP addresses.

35. **Scenario: Reduce failure risk for instances running critical workloads in same AZ. Solution?**  
    Use Spread or Partition placement group.

36. **Scenario: Want low-latency connection for HPC instances in same rack. Solution?**  
    Cluster placement group.

37. **Scenario: Interface endpoint not resolving DNS. Possible cause?**  
    Private DNS not enabled for endpoint.

38. **Scenario: Peering connection shows active but EC2 cannot reach. Possible causes?**  
    Check route tables, overlapping CIDRs, security groups, NACLs.

39. **Scenario: S3 access from private subnet via endpoint not working. Why?**  
    Incorrect route table configuration or missing Gateway Endpoint.

40. **Scenario: EC2 instances require private access to multiple AWS services without internet. How?**  
    Use multiple interface endpoints for each service.

41. **Scenario: Limit EC2 placement group size. Why?**  
    AWS places restrictions based on instance type and AZ for Cluster/Spread.

42. **Scenario: Want to isolate network traffic using multiple NICs. Why?**  
    Security, redundancy, or traffic separation between subnets.

43. **Scenario: VPC Peering costs?**  
    Data transfer between peered VPCs incurs standard inter-AZ or inter-region data transfer charges.

44. **Scenario: Need highly available access to service within VPC. Option?**  
    Interface Endpoint + multiple subnets for redundancy.

45. **Scenario: Placement group change after instance launch. Possible?**  
    Cannot move instance to different placement group after launch; need to create new instance.

46. **Scenario: EC2 in VPC cannot reach endpoint. Checks?**  
    Subnet route table, security group, NACL, private DNS settings.

47. **Scenario: Avoid transitive routing across multiple VPCs. Solution?**  
    Create direct peering between every VPC pair.

48. **Scenario: Multiple NICs on same instance, different AZs. Possible?**  
    Not allowed; NICs must be in same AZ as EC2 instance.

49. **Scenario: Cluster placement group failed to launch all instances. Why?**  
    Insufficient capacity in AZ for requested instance types.

50. **Scenario: You want private connectivity to DynamoDB from VPC without internet. Which endpoint?**  
    Gateway Endpoint.
