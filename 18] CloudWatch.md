## Easy (Basic Understanding)

1. **What is Amazon CloudWatch, and what is its primary purpose?**  
   CloudWatch is a monitoring service for AWS resources and applications.

2. **Name three types of data that CloudWatch can monitor.**  
   Metrics, logs, and events.

3. **What are the three states of a CloudWatch metric alarm?**  
   OK, ALARM, INSUFFICIENT_DATA.

4. **What is the difference between a CloudWatch dashboard and CloudWatch logs?**  
   Dashboards visualize metrics; logs store detailed event or application data.

5. **What type of notification service is integrated with CloudWatch for alerts?**  
   Amazon SNS (Simple Notification Service).

6. **How does CloudWatch get metrics from AWS resources?**  
   AWS services automatically send metrics to CloudWatch.

7. **True or False: CloudWatch can only monitor resources in a single AWS region.**  
   False.

8. **Define what an SNS topic is in the context of CloudWatch.**  
   A communication channel to send notifications to multiple subscribers.

9. **Which AWS service would you use to centralize logs from multiple EC2 instances?**  
   CloudWatch Logs.

10. **What does the INSUFFICIENT_DATA alarm state indicate?**  
    Not enough data is available to determine the alarm state.

## Moderate (Application/Scenario-based)

1. **You notice a CloudWatch alarm in the ALARM state for high CPU utilization. What could be your immediate actions?**  
   Check the instance and scale or optimize resources.

2. **Explain how you would monitor disk I/O performance of an EC2 instance using CloudWatch.**  
   Enable EBS metrics and monitor DiskReadOps/DiskWriteOps.

3. **Describe the steps to create a CloudWatch dashboard showing both EC2 CPU utilization and S3 bucket storage usage.**  
   Create a dashboard → Add widgets for EC2 CPU and S3 metrics.

4. **You need to be notified whenever an RDS database exceeds 80% storage usage. How would you implement this using CloudWatch?**  
   Create a CloudWatch alarm on the metric → Connect it to an SNS topic.

5. **Compare CloudWatch logs vs CloudWatch events. In which scenario would you use each?**  
   Logs for application/system logging; events for operational changes.

6. **How can CloudWatch Events help in automating responses to operational changes? Give an example.**  
   Trigger actions like Lambda functions when an event occurs, e.g., auto-remediate stopped instances.

7. **Scenario: You accidentally deleted a critical configuration file. How can CloudWatch and SNS help you detect and respond quickly?**  
   CloudWatch logs detect deletion → Alarm triggers SNS notification.

8. **What is the relationship between a CloudWatch alarm and an SNS topic?**  
   Alarm sends notifications to subscribers via an SNS topic.

9. **How would you check if a CloudWatch alarm is triggering correctly without waiting for real events?**  
   Manually set the alarm threshold to simulate a trigger.

10. **Scenario: Your EC2 instances are intermittently failing health checks. How could CloudWatch help you identify the root cause?**  
    Monitor metrics/logs for CPU, memory, or network anomalies.

## Hard (Advanced/Conceptual + Complex Scenarios)

1. **Explain how CloudWatch metrics are aggregated across multiple instances and regions.**  
   Metrics can be grouped using namespaces, dimensions, and cross-account dashboards.

2. **Scenario: Your CloudWatch alarm keeps flapping between OK and ALARM states. How would you troubleshoot this “alarm noise”?**  
   Adjust evaluation periods or threshold settings.

3. **Describe the difference between CloudWatch metrics that are standard (5-minute) vs detailed (1-minute). When would you use each?**  
   Standard for low-frequency monitoring; detailed for real-time/critical monitoring.

4. **You want to create a custom metric for monitoring failed login attempts. How would you implement this in CloudWatch?**  
   Publish a custom metric via AWS CLI, SDK, or CloudWatch API.

5. **Scenario: You have multiple AWS accounts. How can CloudWatch centralize monitoring and alerting across accounts?**  
   Use cross-account CloudWatch dashboards and metric sharing.

6. **Explain the cost implications of using CloudWatch detailed monitoring on 50 EC2 instances continuously.**  
   Costs increase per instance for detailed (1-min) metrics and alarms.

7. **Scenario: You want automated scaling based on CloudWatch logs indicating high error rates. How would you design this solution?**  
   Create metric filters → CloudWatch alarm → Trigger Auto Scaling or Lambda.

8. **How does CloudWatch ensure near real-time response in CloudWatch Events, and what are the potential limitations?**  
   Uses event streaming with low latency; limited by event delivery retries and throughput.

9. **Compare using CloudWatch Events vs AWS Lambda for automating incident responses. Provide an example.**  
   Events detect changes, Lambda executes actions; e.g., Event detects EC2 failure → Lambda restarts it.

10. **You need to monitor custom application-level metrics (e.g., active user sessions) and trigger alerts. How would you design this solution?**  
    Publish custom metrics → Create CloudWatch alarm → Connect to SNS → Visualize on dashboard.
