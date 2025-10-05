## Easy Level

1. **What is Amazon EC2?**  
   Amazon Elastic Compute Cloud (EC2) provides scalable virtual servers in the AWS cloud.

2. **What does EC2 stand for?**  
   EC2 stands for Elastic Compute Cloud.

3. **What is the purpose of EC2?**  
   To provide resizable compute capacity to run applications on AWS.

4. **What is an AMI in AWS?**  
   AMI (Amazon Machine Image) is a pre-configured template used to create EC2 instances.

5. **What are the main components of an AMI?**  
   A root volume template, launch permissions, and block device mapping.

6. **What is the default root volume type when launching EC2?**  
   Amazon EBS (Elastic Block Store).

7. **Can an EC2 instance be launched without an AMI?**  
   No, every EC2 instance must be launched from an AMI.

8. **What is Elastic IP in EC2?**  
   A static public IPv4 address associated with an AWS account for consistent access.

9. **Which storage options are available for EC2 instances?**  
   Instance store and Amazon EBS.

10. **What is the default operating system available in AWS EC2?**  
    AWS supports multiple OS options like Amazon Linux, Ubuntu, Windows, etc.
    
## Moderate Level

11. **What are the types of AMIs based on permission?**  
    Public AMI, Private AMI, and AWS Marketplace AMI.

12. **Can we create a custom AMI?**  
    Yes, users can create custom AMIs from existing EC2 instances.

13. **What is the difference between public and private AMIs?**  
    Public AMIs are shared publicly; private AMIs are available only to the owner.

14. **How can we make an AMI available to another AWS account?**  
    By modifying its launch permissions and sharing it with specific account IDs.

15. **What are EC2 instance types used for?**  
    To provide different configurations of CPU, memory, storage, and networking.

16. **What is the default VPC for EC2 instances?**  
    AWS automatically provides a default VPC in each region for EC2 deployment.

17. **What happens when you stop an EC2 instance?**  
    It shuts down, and you can restart it later without losing data stored on EBS.

18. **What happens when you terminate an EC2 instance?**  
    The instance and its attached storage (unless retained) are permanently deleted.

19. **Can you change the instance type after launch?**  
    Yes, you can stop the instance, change its type, and start it again.

20. **What is EC2 User Data used for?**  
    To automate instance configuration or run scripts at boot time.

21. **How do you connect to a Linux EC2 instance?**  
    Using SSH and a key pair (.pem file).

22. **How do you connect to a Windows EC2 instance?**  
    Using Remote Desktop Protocol (RDP) and the decrypted password.

23. **Can one AMI be used across multiple regions?**  
    No, AMIs are region-specific but can be copied to other regions.

24. **What is the pricing model for EC2?**  
    On-Demand, Reserved, Spot, and Dedicated Hosts.

25. **What is the difference between On-Demand and Reserved Instances?**  
    On-Demand has no upfront cost; Reserved requires commitment for lower pricing.

26. **Can you attach multiple volumes to an EC2 instance?**  
    Yes, multiple EBS volumes can be attached to one EC2 instance.

27. **How do you back up an EC2 instance?**  
    By creating an EBS snapshot or custom AMI.

28. **Can an EC2 instance be launched in multiple Availability Zones simultaneously?**  
    No, each EC2 instance resides in one specific Availability Zone.

29. **How do you scale EC2 instances automatically?**  
    Using Auto Scaling Groups (ASG).

30. **What is EC2 instance metadata?**  
    Information about the instance that applications can query from within the instance.
    
## Hard Level

31. **What is the difference between EBS-backed and Instance Store-backed AMIs?**  
    EBS-backed instances persist after stopping; Instance Store-backed do not.

32. **What happens when you reboot an EC2 instance?**  
    It restarts at the OS level, but data and IP addresses remain unchanged.

33. **Can EC2 instances communicate across regions?**  
    Not directly; communication requires inter-region VPC peering or Transit Gateway.

34. **How do you recover a lost private key for EC2?**  
    You can’t; instead, create a new key pair and attach via Systems Manager or recovery process.

35. **What is EC2 Hibernate?**  
    It saves the in-memory state (RAM) to EBS and resumes from there upon restart.

36. **Can you attach an EBS volume from one region to another?**  
    No, you must copy the snapshot to the target region first.

37. **How does EC2 ensure high availability?**  
    By deploying instances across multiple Availability Zones.

38. **What are placement groups in EC2?**  
    Logical groupings to influence instance placement for performance or availability.

39. **Name the three types of placement groups.**  
    Cluster, Spread, and Partition.

40. **What is the use of ENI (Elastic Network Interface)?**  
    It’s a virtual network card for EC2 instances that allows multiple IPs or subnets.

41. **What is the difference between Elastic IP and Public IP?**  
    Public IP changes when instance stops; Elastic IP remains static.

42. **Can EC2 instances use IPv6?**  
    Yes, EC2 supports dual-stack networking with IPv4 and IPv6.

43. **What are EC2 Reserved Instance types?**  
    Standard, Convertible, and Scheduled.

44. **What is Spot Fleet in EC2?**  
    A collection of Spot Instances that meet defined capacity and cost requirements.

45. **How can you monitor EC2 performance?**  
    Using Amazon CloudWatch metrics.

46. **Can you move an EC2 instance from one subnet to another?**  
    Not directly; you must launch a new instance in the target subnet.

47. **What is the default limit of EC2 instances per region?**  
    Usually 20 per region, but limits can be increased upon request.

48. **How can EC2 improve disaster recovery?**  
    By deploying instances across multiple regions and backing up data with snapshots.

49. **What is EC2 Dedicated Host?**  
    Physical server fully dedicated to one customer for compliance or licensing needs.

50. **What’s the difference between EC2 and Lambda?**  
    EC2 provides virtual servers; Lambda runs code serverlessly without managing servers.
