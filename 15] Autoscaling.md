## Easy Level

1. **What is Auto Scaling in AWS?**  
   Auto Scaling automatically adjusts the number of resources (EC2 instances) to meet application demand.

2. **Primary benefits of Auto Scaling?**  
   - Improved performance  
   - Cost efficiency  
   - Reliability

3. **Difference between Horizontal and Vertical Scaling?**  
   - Horizontal Scaling: Add more instances to distribute load.  
   - Vertical Scaling: Increase capacity (CPU, memory, storage) of a single instance.

4. **What is Manual Scaling?**  
   Manually increase or decrease the number of instances via AWS Console or CLI.

5. **What is Dynamic Scaling?**  
   Automatically adjusts the number of instances based on signals like CPU utilization, network traffic, or custom metrics.

6. **Which scaling is better for unpredictable traffic?**  
   Dynamic Scaling.

## Moderate Level

7. **Scenario: Traffic spikes at certain hours. How to handle?**  
   Use Auto Scaling with dynamic scaling policies to add instances during peak hours and remove them during low traffic.

8. **Scenario: You want consistent performance but minimal cost. Solution?**  
   Auto Scaling adjusts resources automatically to match demand, avoiding over-provisioning.

9. **Scenario: Single instance cannot handle increasing load. Solution?**  
   Horizontal Scaling – add more EC2 instances to distribute the load.

10. **Scenario: Upgrade server capacity instead of adding new instances. Which scaling?**  
    Vertical Scaling.

11. **Scenario: Traffic pattern is predictable. Which scaling approach is suitable?**  
    Scheduled Auto Scaling.

12. **Scenario: Auto Scaling not triggered. What to check?**  
    Check scaling policies, CloudWatch alarms, and instance health.

13. **Scenario: You need high availability across AZs. How does Auto Scaling help?**  
    Deploy instances across multiple Availability Zones; Auto Scaling balances resources automatically.

14. **Scenario: You want to scale based on memory usage. How?**  
    Create a custom CloudWatch metric for memory usage and set Auto Scaling policy on it.

15. **Scenario: EC2 instance fails. How Auto Scaling reacts?**  
    Auto Scaling terminates unhealthy instance and launches a new one automatically.

## Hard Level / Scenario-Based

16. **Scenario: Sudden traffic spike causes performance degradation. How Auto Scaling mitigates this?**  
    Dynamic scaling automatically launches additional instances based on metrics like CPU or network traffic to handle the load.

17. **Scenario: Auto Scaling group launches too many instances unnecessarily. How to prevent?**  
    Adjust scaling policies, set cooldown periods, and define upper limits for instance count.

18. **Scenario: Application requires multiple instance types. How to implement?**  
    Create a mixed-instance Auto Scaling group with different EC2 instance types for cost optimization and performance.

19. **Scenario: You want to scale back during low traffic but maintain minimum availability. How?**  
    Configure minimum and maximum instance limits in Auto Scaling group.

20. **Scenario: Scaling based on custom metrics (e.g., queue length). How?**  
    Publish custom metric to CloudWatch and attach it to Auto Scaling policy.

21. **Scenario: Need to test Auto Scaling before production traffic. How?**  
    Simulate load using stress tests or traffic generators to verify scaling policies.

22. **Scenario: Instances across multiple AZs, some AZs fail. How Auto Scaling reacts?**  
    Auto Scaling launches new instances in healthy AZs to maintain desired capacity.

23. **Scenario: Optimize cost with Spot Instances in Auto Scaling. How?**  
    Configure mixed-instance policies with a combination of On-Demand and Spot instances.

24. **Scenario: Application has predictable load every day. How to scale efficiently?**  
    Use scheduled scaling with predefined times to add or remove instances automatically.

25. **Scenario: Scaling triggered too frequently causing instability. How to fix?**  
    Set appropriate cooldown periods and adjust thresholds for scaling metrics.
