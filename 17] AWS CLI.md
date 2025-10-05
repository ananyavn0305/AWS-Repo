## Easy Level

1. **What is AWS CLI?**\
   AWS CLI (Command Line Interface) is a unified tool to manage AWS services from the command line.

2. **How do you configure AWS CLI credentials?**
   ```bash
   aws configure
   You provide AWS Access Key, Secret Key, default region, and output format.

3. **How do you check the AWS CLI version?**
   ```bash
   aws --version

4. **How do you create a key pair using AWS CLI?**
   ```bash
   aws ec2 create-key-pair --key-name MyKeyPair --query 'KeyMaterial' --output text > MyKeyPair.pem
   ```
   Then set permissions: chmod 400 MyKeyPair.pem

5. **How do you SSH into an EC2 instance using a key pair?**
   ssh -i MyKeyPair.pem ec2-user@<instance-public-ip>

## Moderate Level

6. **How do you launch an EC2 instance using AWS CLI?**
   ```bash
   aws ec2 run-instances --image-id ami-xxxxxxxx --count 1 --instance-type t2.micro --key-name MyKeyPair --security-groups MySecurityGroup

7. **How do you create a VPC using AWS CLI?**
   ```bash
   aws ec2 create-vpc --cidr-block 10.0.0.0/16 --output json

8. **How do you create an S3 bucket using AWS CLI?**
   ```bash
   aws s3api create-bucket --bucket <BUCKET_NAME> --region <REGION>

9. **How do you list all EC2 instances using AWS CLI?**
    ```bash
    aws ec2 describe-instances

10. **How do you list all S3 buckets using AWS CLI?**
    ```bash
    aws s3 ls

## Hard Level / Scenario-Based

11. **Scenario: You want to launch multiple EC2 instances at once.**\
    Use --count parameter:
    ```bash
    aws ec2 run-instances --image-id ami-xxxxxxxx --count 3 --instance-type t2.micro --key-name MyKeyPair --security-groups MySecurityGroup

12. **Scenario: You want to create a VPC and automatically get its VPC ID.**
    ```bash
    aws ec2 create-vpc --cidr-block 10.0.0.0/16 --query 'VPC.VPCId' --output text

13. **Scenario: You need to check the public IP of a newly created EC2 instance.**
    ```bash
    aws ec2 describe-instances --query 'Reservations[*].Instances[*].PublicIpAddress' --output text

14. **Scenario: You want to copy files from your local system to S3.**
    ```bash
    aws s3 cp localfile.txt s3://<BUCKET_NAME>/ --region <REGION>
    
15. **Scenario: You need to sync a local folder with an S3 bucket.**
    ```bash
    aws s3 sync /local/folder s3://<BUCKET_NAME>/ --region <REGION>

16. **Scenario: You want to delete an S3 bucket using CLI.**
    ```bash
    aws s3 rb s3://<BUCKET_NAME> --force

17. **Scenario: You want to automate EC2 creation in a script.**
    Use CLI commands inside a shell script or automation tool with parameters for AMI, instance type, key pair, and security group.
