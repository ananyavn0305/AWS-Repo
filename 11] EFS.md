## Easy Level

1. **What is Amazon EFS?**  
   A scalable file storage service that can be accessed by multiple EC2 instances concurrently.

2. **Is EFS block storage or file storage?**  
   File storage.

3. **Can multiple EC2 instances access the same EFS file system simultaneously?**  
   Yes.

4. **Does EFS scale automatically?**  
   Yes, it grows and shrinks based on storage usage.

5. **Can EFS be accessed across multiple Availability Zones?**  
   Yes, within the same region.

6. **What are the two storage classes in EFS?**  
   Standard and Infrequently Accessed (One Zone).

7. **Which EFS storage class is recommended for frequently accessed files?**  
   Standard.

8. **Which EFS storage class is cheaper?**  
   Infrequently Accessed (One Zone).

9. **What protocol does EFS primarily use?**  
   Network File System (NFS).

10. **Does EFS require manual resizing like EBS?**  
    No, it resizes automatically.

## Moderate Level

11. **Scenario: You want low-cost storage for rarely accessed files. Which EFS class?**  
    Infrequently Accessed (One Zone).

12. **Scenario: Multiple EC2 instances in different AZs need access to shared storage. Which service?**  
    Amazon EFS.

13. **What is the main difference between EBS and EFS?**  
    EBS is block storage for single EC2; EFS is file storage for multiple EC2s across AZs.

14. **Scenario: You want a shared file system for web servers. Which AWS service?**  
    Amazon EFS.

15. **What are the performance modes in EFS?**  
    General Purpose and Max I/O.

16. **What are the throughput modes in EFS?**  
    Bursting and Provisioned.

17. **Scenario: How do you mount an EFS file system on EC2?**  
    Install NFS client → create mount directory → mount using `mount -t nfs4 -o nfsvers=4.1 <EFS_DNS>:/ /mnt/efs`.

18. **Scenario: You want to verify EFS is mounted correctly. How?**  
    Use `df -h` command.

19. **Scenario: You need to test file accessibility across two EC2 instances. Steps?**  
    Mount EFS on both → create file → read file from both instances.

20. **Does EFS support cross-region access?**  
    No, only within the same region.

21. **Scenario: EC2 instances don’t have permission to access EFS. How to fix?**  
    Attach an IAM role with `AmazonElasticFileSystemFullAccess`.

22. **Scenario: You need temporary EFS storage. How to clean up?**  
    Unmount → terminate EC2 → delete EFS file system.

23. **What command installs the NFS client on Amazon Linux 2?**  
    `sudo yum -y install nfs-utils`.

24. **Scenario: You want a shared directory `/mnt/efs` on EC2. How to create it?**  
    `sudo mkdir /mnt/efs`.

25. **Scenario: How to write and read a test file in EFS?**  
    `echo "Hello EFS" | sudo tee /mnt/efs/hello.txt` → `cat /mnt/efs/hello.txt`.

26. **Scenario: You want to mount EFS automatically on reboot. Which file to edit?**  
    `/etc/fstab`.

27. **Scenario: EC2 instance cannot access EFS due to NFS errors. What to check?**  
    Security group rules and NFS client installation.

28. **Scenario: How do you delete an EFS file system?**  
    From AWS Console → select EFS → delete.

29. **Scenario: How to attach the same EFS to multiple EC2 instances in the same VPC?**  
    Mount the EFS DNS on each instance.

30. **Scenario: You need highly available file storage across AZs. Which EFS class?**  
    Standard.

## Hard Level / Scenario-Based

31. **Scenario: You need to share files between EC2 Linux and Windows instances. What protocol consideration is there?**  
    EFS supports NFS; Windows may need third-party NFS client.

32. **Scenario: You want to limit costs on infrequently accessed files while keeping them accessible. How?**  
    Use EFS Infrequently Accessed storage class (One Zone).

33. **Scenario: Your EFS is not accessible from EC2. Steps to troubleshoot?**  
    Check Security Groups, NACLs, IAM role permissions, mount commands.

34. **Scenario: Need to back up EFS data. How?**  
    Use AWS Backup or replicate files to S3.

35. **Scenario: Multiple EC2 instances in different subnets need shared storage. Solution?**  
    EFS supports access across subnets in same VPC/AZ.

36. **Scenario: Optimize EFS for thousands of concurrent connections. Which performance mode?**  
    Max I/O.

37. **Scenario: You need consistent low-latency access to frequently used files. Which EFS storage class?**  
    Standard.

38. **Scenario: Automate EFS mounting on multiple EC2 instances during launch. How?**  
    Use EC2 user-data scripts to mount EFS.

39. **Scenario: How to verify if EFS file system is growing automatically?**  
    Check storage metrics via AWS Console or CloudWatch.

40. **Scenario: Two EFS file systems in same VPC, need to separate workloads. How?**  
    Mount each to different directories on EC2.

41. **Scenario: EFS mount fails intermittently. Possible reasons?**  
    NFS client version mismatch, security groups, network issues.

42. **Scenario: You want to copy files from EFS to S3 for archival. Steps?**  
    Use AWS CLI `aws s3 cp` or `aws s3 sync`.

43. **Scenario: Need to monitor EFS throughput and latency. How?**  
    Use CloudWatch metrics: `DataReadBytes`, `DataWriteBytes`, `MetadataIOCount`.

44. **Scenario: Auto-scaling EC2 instances need access to shared storage. Solution?**  
    Mount the same EFS file system on all instances during launch.

45. **Scenario: Limit the number of EC2 instances that can mount an EFS. How?**  
    Control using security groups and network ACLs.

46. **Scenario: Delete an EFS file system but retain data for compliance. How?**  
    Backup data to S3 before deletion.

47. **Scenario: Need a low-latency NFS file system within a single AZ. Which storage class?**  
    Standard or One Zone, depending on cost preference.

48. **Scenario: Automate mounting across multiple AZs. How?**  
    Mount the same EFS DNS name on EC2 instances in each AZ.

49. **Scenario: Security concerns with EFS access. How to mitigate?**  
    Use IAM roles, security groups, and VPC endpoints.

50. **Scenario: Migrate data from EBS to EFS. How?**  
    Attach EBS → copy files to EFS using `cp` or `rsync`.
51. **Scenario: Need versioning of files in EFS for compliance. Solution?**  
    Use AWS Backup with versioning enabled.
