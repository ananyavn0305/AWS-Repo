## Easy Level

1. **What is AWS VPC?**  
   A Virtual Private Cloud is an isolated network environment where you can launch AWS resources with full control over networking.

2. **Can you control IP addressing in a VPC?**  
   Yes, you can define your own CIDR blocks.

3. **What is a subnet?**  
   A subnet is a segment of a VPC's IP address space that helps organize resources and manage traffic.

4. **Types of subnets in VPC?**  
   Public subnet and Private subnet.

5. **What is an Internet Gateway?**  
   A component that allows communication between instances in your VPC and the internet.

6. **What is a NAT Gateway?**  
   Allows instances in private subnets to initiate outbound traffic to the internet while blocking inbound traffic.

7. **What is a route table?**  
   A set of rules that determines where network traffic is directed.

8. **Can you delete the main route table in a VPC?**  
   No, the main route table cannot be deleted.

9. **What is a Security Group in VPC?**  
   A virtual firewall controlling inbound and outbound traffic for EC2 instances.

10. **What is a Network ACL (NACL)?**  
    A firewall controlling inbound and outbound traffic at the subnet level.

## Moderate Level

11. **Scenario: You want an EC2 instance to be publicly accessible. Which subnet?**  
    Public subnet with route to Internet Gateway.

12. **Scenario: Your EC2 instance in a private subnet needs internet access. Solution?**  
    Use a NAT Gateway in a public subnet.

13. **Difference between Security Group and NACL?**  
    Security Groups are stateful and associated with instances; NACLs are stateless and associated with subnets.

14. **Scenario: You need both allow and deny rules at subnet level. Which option?**  
    Network ACL.

15. **Scenario: You want default firewall protection at instance level. Which option?**  
    Security Group.

16. **Scenario: EC2 cannot reach the internet. What to check first?**  
    Subnet route table, Internet Gateway attachment, Security Group rules.

17. **Scenario: Multiple instances in a subnet need independent outbound traffic rules. Which option?**  
    Security Groups (different rules for each instance).

18. **Scenario: You want to isolate subnet traffic completely. Solution?**  
    Use private subnet with NACL restrictions.

19. **What is the default limit of VPCs per region?**  
    5 per region.

20. **What is the default limit of subnets per VPC?**  
    200 per VPC.

21. **Scenario: You want to allow HTTP and HTTPS traffic to an EC2 instance. Security Group rules?**  
    Inbound rules allow ports 80 and 443.

22. **Scenario: A subnet must deny all incoming traffic from a specific IP. Which option?**  
    NACL with deny rule.

23. **Scenario: You need to allow outbound responses automatically after allowing inbound traffic. Which feature helps?**  
    Security Groups are stateful.

24. **Scenario: EC2 instances cannot communicate across subnets in the same VPC. What to check?**  
    Route tables and subnet associations.

25. **Scenario: You want EC2 instances to access the internet via NAT. Which subnet for NAT Gateway?**  
    Public subnet.

26. **Scenario: You want to limit egress traffic from a subnet. Which option?**  
    NACL.

27. **Scenario: Which is evaluated first, Security Group or NACL?**  
    Both are evaluated; NACL at subnet, Security Group at instance level.

28. **Scenario: Multiple instances in same subnet with different rules. How to configure?**  
    Use Security Groups for per-instance control; NACL applies to all.

29. **Scenario: Need to allow inbound SSH but deny all outbound traffic. Which option?**  
    NACL (stateless allows deny rules).

30. **Scenario: Want to attach multiple VPCs together. Which AWS feature?**  
    VPC Peering Connection.

## Hard Level / Scenario-Based

31. **Scenario: EC2 instances in different VPCs need to communicate. Solution?**  
    Use VPC Peering or Transit Gateway.

32. **Scenario: You want fine-grained traffic control at subnet level. Which option?**  
    NACLs with numbered rules.

33. **Scenario: You want highly available NAT Gateway across AZs. How?**  
    Deploy NAT Gateway in each AZ.

34. **Scenario: Security Group rule not taking effect. Possible reasons?**  
    Check rule syntax, protocol, port, and attached instance.

35. **Scenario: NACL inbound rule allowing 80, but outbound not working. Why?**  
    NACLs are stateless; need outbound rule for return traffic.

36. **Scenario: EC2 cannot access the internet even in public subnet. Checks?**  
    Internet Gateway attachment, route table, security group rules.

37. **Scenario: Increase VPC limit beyond default. How?**  
    Submit limit increase request to AWS Support.

38. **Scenario: Restrict certain IPs from accessing subnet while allowing others. Solution?**  
    NACL with allow/deny rules.

39. **Scenario: Multi-tier application, public web servers, private database servers. VPC design?**  
    Public subnet for web servers with IGW; private subnet for DB with NAT for outbound access.

40. **Scenario: EC2 cannot ping another EC2 in same VPC. Checks?**  
    Security Group rules, NACL rules, subnet routing.

41. **Scenario: You want to block all traffic to a subnet temporarily. How?**  
    Update NACL rules to deny inbound and outbound traffic.

42. **Scenario: Multiple EC2 instances need different internet access policies. Which option?**  
    Security Groups per instance.

43. **Scenario: Reduce exposure of private resources to internet. How?**  
    Place resources in private subnets with NAT for outbound.

44. **Scenario: EC2 instance in private subnet requires S3 access without internet. How?**  
    Use VPC Endpoint for S3.

45. **Scenario: Limit number of security groups per instance. What is the default max?**  
    5 per instance.

46. **Scenario: You need isolated test environment in same AWS account. Solution?**  
    Create separate VPC.

47. **Scenario: Evaluate traffic flow from public to private subnet. What AWS tools?**  
    VPC Flow Logs.

48. **Scenario: Need multiple CIDR blocks in a VPC. How?**  
    Add secondary CIDR block to VPC.

49. **Scenario: EC2 instances need external internet for updates, but private. Solution?**  
    Private subnet + NAT Gateway.

50. **Scenario: Block all inbound traffic except specific IPs. Solution?**  
    Security Group with inbound allow rules only for those IPs.
