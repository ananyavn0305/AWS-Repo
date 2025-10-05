## Easy Level

1. **What is SSH?**  
   Secure Shell protocol used for command-line access to Linux EC2 instances.

2. **What is RDP?**  
   Remote Desktop Protocol used for GUI-based access to Windows EC2 instances.

3. **What is the default port for SSH?**  
   22

4. **What is the default port for RDP?**  
   3389

5. **Can SSH be used on Windows?**  
   Yes, using an SSH client like PuTTY or Windows Terminal.

6. **What is a key pair used for in SSH?**  
   Authenticate and securely connect to an EC2 instance without a password.

7. **Can you connect to an EC2 instance without a key pair?**  
   Only if password authentication is enabled (not recommended).

8. **What is a public key?**  
   The part of a key pair stored on the instance for authentication.

9. **What is a private key?**  
   The part of a key pair kept by the user to establish a secure connection.

10. **Which OS requires RDP for remote access?**  
    Windows Server instances.

## Moderate Level

11. **How do you connect to a Linux EC2 instance from macOS?**  
    Using `ssh -i <private-key.pem> ec2-user@<public-ip>` in terminal.

12. **How do you connect to a Windows EC2 instance?**  
    Using RDP client with decrypted Administrator password.

13. **Can multiple users SSH into the same instance?**  
    Yes, by adding multiple public keys to the `authorized_keys` file.

14. **What is the difference between SSH and RDP?**  
    SSH is command-line only; RDP provides a graphical interface.

15. **Scenario: SSH connection fails with “Permission denied (publickey)”. Why?**  
    Incorrect private key, wrong username, or wrong permissions on key file.

16. **Can RDP connections be secured with key pairs?**  
    No, RDP uses username/password; key pairs are for SSH/Linux.

17. **Scenario: Remote connection times out. Possible reasons?**  
    Security group rules, network ACL, wrong IP, or instance not running.

18. **Can you use SSH on a non-standard port?**  
    Yes, by configuring the server and client to use a custom port.

19. **What is the benefit of SSH over password authentication?**  
    More secure, prevents brute-force attacks.

20. **Scenario: RDP shows black screen. What could be wrong?**  
    Instance resources, firewall, RDP configuration, or graphics driver issue.

21. **What OS username is used for Amazon Linux 2?**  
    `ec2-user`

22. **What OS username is used for Ubuntu EC2 instances?**  
    `ubuntu`

23. **What OS username is used for Windows Server EC2 instances?**  
    `Administrator`

24. **Scenario: You lose your private key. How do you access the instance?**  
    Create a new key pair, attach it via another instance or AMI restore.

25. **How can you improve remote access security?**  
    Restrict IPs in security groups, use VPN, or enable multi-factor authentication.

26. **Can RDP connections be limited to certain IP addresses?**  
    Yes, using inbound rules in security groups.

27. **Scenario: SSH is slow or laggy. What could be the cause?**  
    Network latency, high CPU load, or bandwidth limitations.

28. **Can you configure SSH for key rotation?**  
    Yes, periodically replace keys and update `authorized_keys`.

29. **Scenario: You need to access multiple Linux instances securely. What’s recommended?**  
    Use a bastion host or AWS Systems Manager Session Manager.

30. **Can you monitor active remote sessions on EC2?**  
    Yes, using system logs or AWS CloudTrail.

## Hard Level

31. **What is a bastion host?**  
    A special EC2 instance used as a secure entry point to other instances.

32. **Scenario: Your instance is in a private subnet. How do you access it remotely?**  
    Use a bastion host in a public subnet or Systems Manager Session Manager.

33. **What is port forwarding in SSH?**  
    Redirecting network traffic through a secure SSH tunnel.

34. **Scenario: You need secure file transfer to EC2. What protocols can you use?**  
    SCP, SFTP, or AWS Transfer Family.

35. **How can you restrict SSH access to corporate IPs?**  
    Configure security group inbound rule to allow port 22 from corporate IPs.

36. **Scenario: Multiple users require temporary SSH access. How do you manage it securely?**  
    Use IAM roles, temporary certificates, or Systems Manager Session Manager.

37. **Can you use AWS Systems Manager Session Manager instead of SSH/RDP?**  
    Yes, it provides secure shell access without opening ports.

38. **Scenario: SSH key is compromised. What should you do?**  
    Remove the public key from `authorized_keys` and replace it with a new key.

39. **Can RDP traffic be encrypted?**  
    Yes, RDP supports encryption using TLS.

40. **Scenario: Remote Linux instance becomes unresponsive. How do you troubleshoot?**  
    Check CloudWatch metrics, system logs, or use Systems Manager to access it.

41. **Can you audit remote access to instances?**  
    Yes, using AWS CloudTrail or OS-level logs.

42. **Scenario: SSH connection requires multi-factor authentication. How can it be implemented?**  
    Use AWS IAM or PAM modules supporting MFA.

43. **Scenario: You want to access EC2 without opening ports to the internet. How?**  
    Use VPN, Direct Connect, or Session Manager.

44. **What is the difference between RDP over the internet and over VPN?**  
    VPN provides secure encrypted tunnel, while RDP over internet exposes ports.

45. **Scenario: User reports “Connection refused” for SSH. Possible causes?**  
    SSH daemon not running, firewall blocking port, security group misconfigured.

46. **Scenario: You need to access Windows GUI from Linux workstation. How?**  
    Use an RDP client compatible with Linux.

47. **How can you improve remote access security for multiple instances?**  
    Use centralized bastion, key management, and audit logs.

48. **Scenario: You want temporary access for contractors. How do you achieve this?**  
    Create temporary IAM user, provide limited key pair access, remove after duration.

49. **Scenario: Remote access logs need to be centrally monitored. How?**  
    Forward SSH/RDP logs to CloudWatch or SIEM tool.

50. **What are best practices for EC2 remote access security?**  
    Use key pairs, restrict IPs, enable MFA, use Session Manager, and monitor logs.
