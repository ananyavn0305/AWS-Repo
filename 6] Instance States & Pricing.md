## Easy Level

1. **What are EC2 instance states?**  
   States that describe the lifecycle of an EC2 instance (Pending, Running, Stopped, Terminated, etc.).

2. **What is the Pending state?**  
   The instance is launching but not yet ready for use.

3. **What is the Running state?**  
   The instance is fully operational and can be accessed.

4. **What is the Stopping state?**  
   The instance is in the process of shutting down.

5. **What is the Stopped state?**  
   The instance is shut down and not running; EBS volumes persist.

6. **What is the Terminating state?**  
   The instance is shutting down and will soon be deleted.

7. **What is the Terminated state?**  
   The instance is permanently deleted and cannot be restarted.

8. **What is the Hibernating state?**  
   The instance saves in-memory data to EBS and stops, resuming later.

9. **How do you move an instance from Stopped to Running?**  
   Simply start the instance from the AWS Console or CLI.

10. **Do you incur charges when an instance is stopped?**  
    No, only storage (EBS) is charged; instance usage is free.

## Moderate Level

11. **Can you stop and start an instance multiple times?**  
    Yes, you can stop and start as many times as needed.

12. **What happens to the public IP when an instance is stopped?**  
    The public IP changes unless an Elastic IP is associated.

13. **Scenario: Your instance is stuck in Pending state. What could be the reason?**  
    Resource limits, unavailable instance type in AZ, or network issues.

14. **What is the difference between Stopping and Terminating an instance?**  
    Stopping preserves the EBS root volume; Terminating deletes the instance and storage.

15. **What is On-Demand pricing in EC2?**  
    Pay by the hour or second with no long-term commitment.

16. **What is Reserved Instance pricing?**  
    Pay upfront or partially for a 1- or 3-year term at a discount.

17. **What is Spot Instance pricing?**  
    Buy unused capacity at a discounted rate; can be interrupted by AWS.

18. **What is the Savings Plan pricing model?**  
    Commit to a consistent usage level for 1–3 years in exchange for savings.

19. **What is a Dedicated Host in EC2?**  
    A physical server dedicated to a single customer for compliance or licensing.

20. **Can an instance move between On-Demand and Reserved pricing?**  
    No, Reserved Instances must be launched separately or converted within same family.

21. **What is the benefit of Reserved Instances?**  
    Cost savings up to 75% compared to On-Demand.

22. **Which pricing model is best for flexible, short-term workloads?**  
    On-Demand Instances.

23. **Which pricing model is best for predictable, long-term workloads?**  
    Reserved Instances or Savings Plans.

24. **Which pricing model is best for fault-tolerant, flexible workloads?**  
    Spot Instances.

25. **Do Dedicated Hosts incur additional costs?**  
    Yes, you pay for the entire host regardless of instance usage.

26. **Can Spot Instances be terminated by AWS?**  
    Yes, if capacity is needed elsewhere, usually with a 2-minute warning.

27. **How is Hibernation charged?**  
    Only for EBS storage; instance-hour charges pause while hibernated.

28. **What happens to instance store volumes when an instance stops?**  
    Data is lost; instance store is ephemeral storage.

29. **Scenario: You need minimal EC2 cost for a dev environment. Which pricing model?**  
    Spot Instances or On-Demand with small instance size.

30. **Scenario: You need 24/7 availability with predictable usage. Which pricing model?**  
    Reserved Instances or Savings Plan.

## Hard Level

31. **What is the difference between Reserved Instances and Savings Plans?**  
    Reserved Instances reserve capacity; Savings Plans provide flexible cost savings.

32. **Scenario: An instance is stuck in Stopping state. How would you troubleshoot?**  
    Check dependencies like attached EBS volumes, network interfaces, or AWS service status.

33. **Scenario: Terminated instance accidentally deleted critical data. How can you recover it?**  
    Restore from EBS snapshots or AMI backups.

34. **What are the lifecycle transitions of an EC2 instance?**  
    Pending → Running → Stopping → Stopped → Starting → Running → Terminating → Terminated.

35. **Scenario: You want to minimize costs for batch processing jobs. Which pricing model?**  
    Spot Instances with flexible start and end times.

36. **What is the maximum duration for a Spot Instance?**  
    No hard limit, but AWS may terminate based on capacity or bid price.

37. **How does EC2 pricing vary by region?**  
    Prices differ due to infrastructure cost and demand in each region.

38. **Scenario: Hibernating instance fails to resume. What could be the reason?**  
    Insufficient EBS storage, incompatible OS, or instance type unsupported.

39. **Can you convert a running On-Demand instance to Reserved?**  
    No; Reserved must be purchased separately or apply credits for future usage.

40. **Scenario: You have multiple instances and want cost transparency. How do you track it?**  
    Use AWS Cost Explorer and CloudWatch billing metrics.

41. **What is the impact of stopping an instance with multiple EBS volumes?**  
    All EBS volumes persist; instance store volumes are lost.

42. **Scenario: Reserved Instance is not fully utilized. How can you optimize cost?**  
    Modify or exchange Reserved Instance to match usage.

43. **Can EC2 pricing be affected by instance type and size?**  
    Yes, larger and higher-performance instances cost more per hour.

44. **Scenario: You want a guaranteed physical server for licensing. Which option?**  
    Dedicated Host.

45. **Scenario: You want cost flexibility across different instance types. Which option?**  
    Savings Plans.

46. **How are instance-hours calculated for partial-hour usage?**  
    EC2 bills per second (Linux) or per hour (Windows) depending on OS.

47. **Scenario: You have a short-term experiment that may run anytime in the month. Which pricing model?**  
    Spot Instances for minimal cost.

48. **What is the impact of region selection on pricing?**  
    Some regions are cheaper due to lower infrastructure costs.

49. **Scenario: Instance needs to resume exactly as before after a stop. Which state?**  
    Hibernating instance saves in-memory data for exact resume.

50. **Why is it recommended to monitor EC2 costs regularly?**  
    To avoid unexpected charges, optimize resources, and choose the best pricing model.
