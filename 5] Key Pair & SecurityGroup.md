## Easy Level

1. **What is an EC2 key pair?**  
   A set of security credentials (public and private keys) to securely access EC2 instances.

2. **What is the purpose of the public key?**  
   It is stored on the instance to authenticate incoming connections.

3. **What is the purpose of the private key?**  
   It is used by the user to securely connect to the instance; must be kept secret.

4. **How do you create a key pair in AWS?**  
   Through AWS Management Console, CLI, or SDK.

5. **Which file type is used for a private key?**  
   `.pem` for Linux/Mac or `.ppk` for Windows (PuTTY).

6. **Can a private key be regenerated if lost?**  
   No; you must create a new key pair and update instances.

7. **What is a security group in AWS?**  
   A virtual firewall controlling inbound and outbound traffic to EC2 instances.

8. **What is an inbound rule in a security group?**  
   Specifies what incoming traffic is allowed to reach the instance.

9. **What is an outbound rule in a security group?**  
   Specifies what outgoing traffic is allowed from the instance.

10. **Can security groups be attached to multiple instances?**  
    Yes, one security group can be associated with multiple instances.

## Moderate Level

11. **Can security groups allow or block traffic by IP address?**  
    Yes, you can specify allowed or blocked IP ranges in rules.

12. **Are security groups stateful or stateless?**  
    Stateful — return traffic is automatically allowed, regardless of outbound rules.

13. **How do you connect to a Linux instance using a key pair?**  
    Using SSH with the private key file.

14. **How do you connect to a Windows instance using a key pair?**  
    Using RDP with the decrypted password from the key pair.

15. **Can security groups filter traffic by port?**  
    Yes, inbound and outbound rules can specify TCP/UDP ports.

16. **What happens if no security group is assigned to an EC2 instance?**  
    AWS assigns the default security group of the VPC.

17. **Can you edit a security group after creation?**  
    Yes, you can modify inbound and outbound rules anytime.

18. **What is the difference between a security group and a network ACL?**  
    Security groups are stateful at instance level; NACLs are stateless at subnet level.

19. **What is SSH port default number?**  
    Port 22.

20. **What is RDP port default number?**  
    Port 3389.

21. **Can a key pair be shared across multiple AWS accounts?**  
    Not directly; you must create separate key pairs or share AMIs with embedded keys.

22. **Can multiple key pairs be assigned to a single EC2 instance?**  
    Yes, multiple public keys can be added to the `authorized_keys` file.

23. **What is the best practice for private key storage?**  
    Keep it secure offline or in a secure vault; do not share publicly.

24. **Can security groups reference other security groups?**  
    Yes, inbound rules can allow traffic from other security groups.

25. **What is the difference between default and custom security groups?**  
    Default allows all outbound and limited inbound; custom starts with no rules.

26. **What is a key pair rotation?**  
    Periodically replacing old key pairs with new ones for enhanced security.

27. **How do you troubleshoot key pair connection errors?**  
    Check private key permissions, user name, instance public IP, and security group rules.

28. **Can a security group allow traffic from anywhere?**  
    Yes, by setting `0.0.0.0/0` for IPv4 or `::/0` for IPv6.

29. **What is the significance of security group priority?**  
    Security groups do not have priority; all rules are evaluated collectively.

30. **What happens if you remove a public key from an instance?**  
    Connections using the corresponding private key will no longer work.

## Hard Level

31. **Scenario: You cannot SSH into your Linux instance. What could be the reasons?**  
    Incorrect key, wrong username, missing security group rule, instance not running, or wrong IP.

32. **Scenario: Multiple users need access to one EC2 instance. How do you provide it securely?**  
    Add their public keys to the `authorized_keys` file or use AWS Systems Manager Session Manager.

33. **Scenario: You want to allow web traffic only from a specific office IP. How?**  
    Set inbound rule in the security group allowing TCP port 80 from that IP range.

34. **Scenario: RDP fails to connect to Windows instance. What steps would you take?**  
    Check security group rules, Windows firewall, network ACLs, public IP, and RDP client configuration.

35. **How do you revoke access to an instance immediately?**  
    Remove the user’s public key or modify security group to block their IP.

36. **Scenario: Your security group has 0 inbound rules. Can you connect to the instance?**  
    No, all inbound traffic is blocked by default.

37. **Scenario: Multiple security groups attached to one instance. How are rules evaluated?**  
    Rules are combined; traffic is allowed if any rule permits it.

38. **How do you restrict SSH access to a specific subnet?**  
    Set the security group inbound rule to allow port 22 from the subnet CIDR.

39. **What is a security risk if you set 0.0.0.0/0 for SSH inbound?**  
    It exposes the instance to attacks from anywhere on the internet.

40. **Scenario: Lost private key, but instance must remain accessible. How do you fix?**  
    Create a new key pair, stop the instance, mount the root volume to another instance, replace `authorized_keys`.

41. **Can you use multiple security groups to separate different services on same instance?**  
    Yes, you can attach multiple SGs to control traffic per service port.

42. **What is the difference between security group and IAM roles?**  
    Security groups control network access; IAM roles control API/service permissions.

43. **How can security groups help in compliance?**  
    Restricting access to sensitive instances based on IP, ports, or services.

44. **Scenario: Two instances in different VPCs need communication. How do security groups play a role?**  
    Security groups allow inbound/outbound traffic; VPC peering or VPN is also required.

45. **Can you assign a security group to a running instance?**  
    Yes, changes take effect immediately.

46. **What is the default SSH username for Amazon Linux 2?**  
    `ec2-user`.

47. **What is the default RDP username for Windows Server?**  
    `Administrator`.

48. **Scenario: Security group misconfiguration blocks application traffic. How do you fix?**  
    Review and update inbound/outbound rules with correct ports and IPs.

49. **What is the difference between instance-level and subnet-level access control?**  
    Security groups are instance-level; NACLs are subnet-level and stateless.

50. **Scenario: You need to enforce strict network security for EC2. Which features would you use?**  
    Security groups, NACLs, key pairs, VPN, private subnets, and monitoring tools.
