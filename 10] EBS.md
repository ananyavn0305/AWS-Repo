## Easy Level

1. **What is Amazon EBS?**  
   A block-level storage service for use with Amazon EC2 instances.

2. **Are EBS volumes persistent?**  
   Yes, they remain available even if the EC2 instance is stopped or terminated.

3. **Can an EBS volume attach to multiple EC2 instances at the same time?**  
   No, only one instance at a time.

4. **Do EBS volumes and EC2 instances need to be in the same AZ?**  
   Yes, both must be in the same Availability Zone.

5. **Name the three types of EBS volumes.**  
   SSD, HDD, Magnetic Standard.

6. **Which EBS volume type is bootable?**  
   SSD.

7. **What is GP2 in EBS?**  
   General Purpose SSD volume type with a balance of price and performance.

8. **What is io1 or io2 volume type?**  
   Provisioned IOPS SSD for I/O-intensive workloads.

9. **What is the use of st1 EBS volume?**  
   Throughput Optimized HDD for large, sequential data access.

10. **What is sc1 EBS volume?**  
    Cold HDD for infrequently accessed workloads.

## Moderate Level

11. **What is an EBS snapshot?**  
    Backup of an EBS volume capturing its state at a specific time.

12. **Are EBS snapshots incremental?**  
    Yes, only the changed blocks are saved.

13. **Can snapshots be used for disaster recovery?**  
    Yes, or to migrate data across regions/accounts.

14. **What does EBS encryption protect?**  
    Data at rest, data in transit, snapshots, and volumes created from snapshots.

15. **Scenario: You need high IOPS for a database. Which volume would you choose?**  
    Provisioned IOPS SSD (io1/io2).

16. **Scenario: You want a low-cost volume for infrequently accessed logs. Which volume?**  
    Cold HDD (sc1) or Magnetic Standard.

17. **How do you create partitions on a newly attached EBS volume?**  
    Use `fdisk` to create partitions.

18. **How do you format an EBS partition?**  
    Using `mkfs` command, e.g., `sudo mkfs.ext4 /dev/xvdf1`.

19. **What is a mount point in EBS?**  
    Directory where a partition is attached to access its files.

20. **What is the purpose of UUID in EBS?**  
    To uniquely identify storage devices and partitions.

21. **Scenario: You want your EBS volume to mount automatically after reboot. What do you do?**  
    Add the volume entry in `/etc/fstab` using its UUID.

22. **Can EBS volumes be resized after creation?**  
    Yes, you can increase size and adjust partitions accordingly.

23. **What command lists attached block devices?**  
    `lsblk`.

24. **Scenario: You need to attach the same EBS snapshot to multiple instances. Can you do it directly?**  
    No, create separate volumes from the snapshot.

25. **What is the difference between GP2 and GP3?**  
    GP3 is cheaper and allows independent IOPS provisioning.

26. **Scenario: You need high throughput for large sequential files. Which volume type?**  
    Throughput Optimized HDD (st1).

27. **Which volume type is recommended for boot volumes?**  
    General Purpose SSD (GP2/GP3).

28. **What happens if you delete an instance? Are attached EBS volumes deleted?**  
    Depends on the “Delete on Termination” flag; if set, the volume is deleted.

29. **Scenario: You want to migrate an EBS volume to another region. How?**  
    Create a snapshot and copy it to the target region.

30. **Are Magnetic Standard volumes still recommended?**  
    Only for legacy workloads or small infrequent access data.

## Hard Level / Scenario-Based

31. **Scenario: How do you optimize cost for a high I/O database?**  
    Use Provisioned IOPS SSD with precise IOPS provisioning.

32. **Scenario: Your EBS volume fails during read/write. How do you recover?**  
    Use latest snapshot to create a new volume.

33. **Scenario: You need an EBS volume to attach to multiple instances simultaneously. How?**  
    Use EBS Multi-Attach (only for io1/io2 Block Express volumes).

34. **Scenario: You need encrypted EBS volumes for compliance. How do you ensure encryption at rest?**  
    Enable encryption when creating the volume and use KMS-managed keys.

35. **Scenario: You want to copy EBS snapshots between AWS accounts. How?**  
    Share snapshot with target account and create a volume from it.

36. **Scenario: How do you increase IOPS on an existing GP3 volume?**  
    Modify the volume through AWS console/CLI to adjust IOPS.

37. **Scenario: Partition and mount a new 1TB EBS volume on Linux. Steps?**  
    Attach volume → `lsblk` → `fdisk` → create partition → `mkfs` → mount → update `/etc/fstab`.

38. **Scenario: You want high-speed storage for a machine learning workload. Which volume type?**  
    Provisioned IOPS SSD (io2 Block Express).

39. **Scenario: You need to back up only changed blocks of a large volume daily. How?**  
    Use incremental EBS snapshots.

40. **Scenario: You accidentally detach an EBS volume without unmounting. What happens?**  
    Potential data corruption; use `fsck` to check filesystem integrity.

41. **Scenario: Your EC2 instance is in AZ A, but your EBS volume is in AZ B. Can you attach it?**  
    No, volumes must be in the same Availability Zone.

42. **Scenario: You want to minimize latency for database workloads. Which EBS type?**  
    SSD, preferably Provisioned IOPS SSD.

43. **Scenario: Automate mounting EBS volumes across multiple instances. How?**  
    Use CloudFormation or user-data scripts with `/etc/fstab` entries.

44. **Scenario: Volume exceeds allocated IOPS during peak traffic. What happens?**  
    Performance may be throttled until usage falls below the baseline or IOPS is increased.

45. **Scenario: Need disaster recovery in a different region. Approach?**  
    Copy snapshots to target region and create new volumes.

46. **Scenario: You need to encrypt an existing unencrypted EBS volume. How?**  
    Take a snapshot, encrypt it, and create a new volume from the encrypted snapshot.

47. **Scenario: You want to reduce storage costs of inactive volumes. How?**  
    Take snapshots and delete idle volumes.

48. **Scenario: Multi-volume EC2 instance needs data segregation. How?**  
    Partition volumes logically and mount at different mount points.

49. **Scenario: How to monitor EBS performance and IOPS usage?**  
    Use CloudWatch metrics like VolumeReadOps, VolumeWriteOps, and Throughput.

50. **Scenario: How to recover from accidental deletion of a volume?**  
    Restore from latest snapshot backup.

51. **Scenario: Need to share snapshot between regions securely. How?**  
    Copy snapshot to another region and apply KMS encryption.
52. **Scenario: EBS volume needs resizing and partition expansion without downtime. How?**  
    Modify volume in AWS console and use `resize2fs` on Linux.
