## Easy (Basic Understanding)

1. **What is AWS CLI used for?**  
   - To manage AWS services from the command line.

2. **Which command is used to configure AWS CLI credentials?**  
   - `aws configure`.

3. **How do you launch an EC2 instance using AWS CLI?**  
   - Use `aws ec2 run-instances` with image ID, instance type, key, and security group.

4. **How do you create a key pair using AWS CLI?**  
   - `aws ec2 create-key-pair --key-name <KeyName>`.

5. **Which command is used to set permissions for a private key file?**  
   - `chmod 400 MyKeyPair.pem`.

6. **How do you SSH into an EC2 instance using the key pair?**  
   - `ssh -i MyKeyPair.pem ec2-user@<instance-public-ip>`.

7. **Which AWS CLI command is used to create a VPC?**  
   - `aws ec2 create-vpc --cidr-block <CIDR>`.

8. **How do you create an S3 bucket via AWS CLI?**  
   - `aws s3api create-bucket --bucket <BucketName> --region <Region>`.

9. **True or False: AWS CLI can be used to manage all AWS services.**  
   - True.

10. **What file stores the AWS CLI configuration by default?**  
    - `~/.aws/credentials` and `~/.aws/config`.

## Moderate (Application/Scenario-based)

1. **You want to launch multiple EC2 instances in a single command. Which parameter would you use?**  
   - `--count`.

2. **Scenario: You forgot your key-pair permissions are too open. What will happen if you SSH into EC2?**  
   - SSH will fail due to insecure private key permissions.

3. **How do you specify which region to create AWS resources using CLI?**  
   - Use `--region <Region>` parameter or `aws configure`.

4. **Scenario: You want to create a bucket in a region other than default. Which CLI command would you run?**  
   - `aws s3api create-bucket --bucket <BucketName> --region <Region>`.

5. **How can you list all S3 buckets using AWS CLI?**  
   - `aws s3 ls`.

6. **Scenario: You accidentally launched an instance in the wrong region. How can you terminate it using CLI?**  
   - `aws ec2 terminate-instances --instance-ids <InstanceID> --region <Region>`.

7. **How do you check the public IP of an EC2 instance using CLI?**  
   - `aws ec2 describe-instances --query 'Reservations[*].Instances[*].PublicIpAddress'`.

8. **Scenario: You need to create a key-pair and immediately SSH into EC2. Outline the steps.**  
   - `create-key-pair` → save PEM → `chmod 400` → `ssh -i`.

9. **How do you run CLI commands without entering credentials every time?**  
   - Use `aws configure` to save access key and secret key.

10. **Scenario: You need to automate EC2 instance creation in a script. Which AWS CLI parameters are essential?**  
    - `--image-id`, `--instance-type`, `--key-name`, `--security-groups`, `--count`.

## Hard (Advanced/Conceptual + Complex Scenarios)

1. **Scenario: You want to launch an EC2 instance with a specific IAM role using CLI. How?**  
   - Use `--iam-instance-profile Name=<RoleName>`.

2. **Explain the difference between `aws s3` and `aws s3api` commands.**  
   - `aws s3` is high-level; `aws s3api` is low-level with full API control.

3. **Scenario: You need to copy a local folder to an S3 bucket recursively. Which CLI command will you use?**  
   - `aws s3 cp <local_path> s3://<bucket_name> --recursive`.

4. **How can you configure AWS CLI to use a profile for multiple AWS accounts?**  
   - Use `aws configure --profile <profile_name>` and `--profile <profile>` in commands.

5. **Scenario: You want to tag an EC2 instance at creation using CLI. Which parameter do you use?**  
   - `--tag-specifications 'ResourceType=instance,Tags=[{Key=Name,Value=MyInstance}]'`.

6. **Explain the use of `--query` in AWS CLI.**  
   - Filters CLI output using JMESPath expressions.

7. **Scenario: You want to launch EC2 instances in a specific subnet via CLI. How would you do it?**  
   - Use `--subnet-id <SubnetID>` parameter in `run-instances`.

8. **Scenario: You want to enable versioning for an S3 bucket using CLI. How?**  
   - `aws s3api put-bucket-versioning --bucket <BucketName> --versioning-configuration Status=Enabled`.

9. **How do you delete all objects in an S3 bucket using CLI before deleting the bucket itself?**  
   - `aws s3 rm s3://<BucketName> --recursive`.

10. **Scenario: Automating EC2 instance launch and monitoring requires CLI and CloudWatch integration. Outline the steps.**  
    - Launch instance → attach IAM role → configure CloudWatch metrics → set alarms using CLI.
