## Easy Level

1. **What is an Amazon Machine Image (AMI)?**  
   A pre-configured template used to launch EC2 instances.

2. **What components make up an AMI?**  
   Root volume template, launch permissions, block device mappings.

3. **What is a root volume template?**  
   The primary storage containing OS and pre-installed software.

4. **What are launch permissions in an AMI?**  
   Define who can use the AMI to launch instances.

5. **What are block device mappings?**  
   Define additional storage volumes attached to an instance at launch.

6. **Name the four types of AMIs.**  
   Amazon-provided, Marketplace, Community, Custom.

7. **What is a Marketplace AMI?**  
   Created by third-party vendors and available on AWS Marketplace.

8. **What is a Community AMI?**  
   Shared by other AWS users, often free to use.

9. **What is a Custom AMI?**  
   Created by you or your organization with tailored configurations.

10. **What is the purpose of a status check in EC2?**  
    To monitor the health of instances and detect hardware/software issues.

## Moderate Level

11. **How many types of status checks are there in EC2?**  
    Three: System, Instance, and Attached EBS status checks.

12. **What does a System Status Check monitor?**  
    The AWS infrastructure hosting your instance (hardware/network).

13. **What does an Instance Status Check monitor?**  
    Software and network configuration of the individual EC2 instance.

14. **What is an Attached EBS status check?**  
    Checks the health and I/O of attached EBS volumes.

15. **Scenario: System status check fails. What could be the reason?**  
    Loss of network connectivity, hardware failure, or host power issue.

16. **Scenario: Instance status check fails. Possible causes?**  
    Exhausted memory, corrupted file system, incorrect networking or kernel issues.

17. **Scenario: Attached EBS status check fails. What might happen?**  
    Instance cannot perform read/write operations on the EBS volume.

18. **Can you view status check results in the AWS console?**  
    Yes, under the EC2 instance “Status Checks” tab.

19. **Scenario: You want to automate AMI launches with predefined settings. What AWS feature would you use?**  
    Launch templates.

20. **What is the benefit of using a launch template?**  
    Saves time and ensures consistent instance configurations.

21. **Can you create multiple instances from a single AMI?**  
    Yes, to launch multiple instances with the same configuration.

22. **Can you modify an Amazon-provided AMI?**  
    No, but you can create a Custom AMI from it.

23. **Scenario: Need software pre-installed on all instances. How can you achieve this?**  
    Create a Custom AMI with the required software.

24. **Can Marketplace AMIs be free?**  
    Some may be free; others require purchase or subscription.

25. **What is the difference between System and Instance status checks?**  
    System checks the AWS host; Instance checks your virtual machine software/configuration.

26. **What is the metric for System Status Check failure?**  
    `StatusCheckFailed_System`

27. **What is the metric for Instance Status Check failure?**  
    `StatusCheckFailed_Instance`

28. **What is the metric for Attached EBS Status Check failure?**  
    `StatusCheckFailed_AttachedEBS`

29. **Scenario: Instance is running but cannot connect. Which status check should you check first?**  
    Instance status check.

30. **Scenario: EC2 cannot perform I/O on a volume. Which status check indicates this?**  
    Attached EBS status check.

## Hard Level

31. **Scenario: How do you troubleshoot a failed System Status Check?**  
    Wait for AWS to resolve, or stop/start the instance if instructed.

32. **Scenario: Instance status check repeatedly fails after reboot. What steps would you take?**  
    Check networking, disk space, memory, kernel compatibility, and OS configuration.

33. **Scenario: Attached EBS fails but instance is healthy. How do you resolve it?**  
    Check EBS volume health, detach/reattach, or restore from snapshot.

34. **How can you create a Custom AMI from an existing instance?**  
    Stop the instance, then create an AMI from the AWS console or CLI.

35. **Scenario: Need to launch multiple identical instances across regions. How can you do this?**  
    Copy the AMI to target regions and use launch templates for automation.

36. **Scenario: Status check fails, but instance continues to run. What does it imply?**  
    There may be minor hardware/software issues; AWS recommends monitoring or corrective actions.

37. **How can you automate instance launches with AMI and predefined configuration?**  
    Use Launch Templates with instance type, storage, AMI, and tags defined.

38. **Scenario: Launch template needs to be updated with new AMI. How do you do it?**  
    Create a new version of the launch template with the updated AMI.

39. **Scenario: Custom AMI is shared with another AWS account. What permissions are required?**  
    Set launch permissions for that account.

40. **What are the advantages of using a launch template over manual instance launch?**  
    Consistency, speed, versioning, and automation support.

41. **Scenario: You need to recover an instance from a failed status check. What are the options?**  
    Stop/start the instance, detach and reattach EBS volumes, or restore from snapshot.

42. **Scenario: You want to use a pre-installed database on multiple instances. Which AMI type is suitable?**  
    Custom AMI or Marketplace AMI with the database installed.

43. **Can launch templates include security group and key pair configuration?**  
    Yes, along with network settings, storage, and tags.

44. **Scenario: EC2 fails both system and instance status checks. What is the recommended action?**  
    Stop/start the instance or contact AWS support if system issues persist.

45. **Scenario: How do you ensure zero-downtime deployment with new AMIs?**  
    Launch new instances with the updated AMI, test, and shift traffic gradually.

46. **Scenario: Instance status check shows “Impaired.” What does it mean?**  
    The instance has a problem with software, configuration, or resource exhaustion.

47. **Scenario: EBS volume attached to multiple instances. How do you monitor status?**  
    Use attached EBS status check for each instance and CloudWatch metrics.

48. **Scenario: Need to maintain AMI versions. How is this achieved?**  
    Use versioning naming conventions and launch templates with version selection.

49. **Scenario: How to recover a failed custom AMI deployment?**  
    Revert to previous AMI version or restore from backup snapshot.

50. **Scenario: Automating multi-region deployment with AMIs and launch templates. What are the steps?**  
    Copy AMIs to target regions, create launch templates, define parameters, and launch instances programmatically.
