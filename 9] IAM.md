## Easy Level

1. **What is AWS IAM?**  
   A service that securely manages access to AWS resources.

2. **What is the difference between authentication and authorization?**  
   Authentication verifies identity; authorization determines permissions.

3. **What principle does IAM follow?**  
   Principle of Least Privilege.

4. **What is an IAM user?**  
   An entity representing a person needing access to AWS resources.

5. **What is an IAM group?**  
   A collection of users that inherit permissions assigned to the group.

6. **Can users belong to multiple IAM groups?**  
   Yes.

7. **Can groups belong to other groups in IAM?**  
   No.

8. **What is an IAM policy?**  
   A JSON document specifying permissions for AWS resources.

9. **Can IAM policies be attached to roles?**  
   Yes, as well as to users and groups.

10. **What are AWS Managed Policies?**  
    Predefined policies maintained by AWS.

## Moderate Level

11. **What are Customer Managed Policies?**  
    Policies created and managed by the user or organization.

12. **What is an Inline Policy?**  
    A policy created for a single IAM identity, not reusable.

13. **What is an IAM role?**  
    A set of permissions that can be assigned to AWS services or users.

14. **Scenario: You want multiple EC2 instances to access S3. How do you do it?**  
    Assign an IAM role to the EC2 instances with S3 permissions.

15. **What is MFA in AWS?**  
    Multi-Factor Authentication requiring a second form of verification.

16. **Can MFA be enabled for root AWS accounts?**  
    Yes, it is recommended.

17. **Scenario: You want to give read-only access to multiple users for S3. What should you do?**  
    Create a group, attach AmazonS3ReadOnlyAccess policy, add users to the group.

18. **What is the difference between Managed and Inline policies?**  
    Managed policies are reusable; Inline policies are attached to a single identity.

19. **Scenario: A user cannot access a resource. How do you troubleshoot?**  
    Check attached policies, group permissions, and explicit deny rules.

20. **Can an IAM user have multiple policies attached?**  
    Yes.

21. **What happens to inline policies if a user is deleted?**  
    Inline policies are deleted along with the user.

22. **Can IAM roles be assumed by users from other AWS accounts?**  
    Yes, with proper trust policies.

23. **Scenario: You need temporary access for an external auditor. How do you provide it?**  
    Create an IAM role with limited permissions and share temporary credentials.

24. **Can IAM groups have policies attached?**  
    Yes, managed or inline policies can be attached to groups.

25. **Scenario: How do you grant cross-account access to an S3 bucket?**  
    Use IAM roles and trust policies for the other account.

26. **What is the main advantage of using IAM roles over IAM users?**  
    Roles provide temporary credentials and are more secure for services.

27. **Can IAM roles be assumed by AWS services?**  
    Yes, such as EC2, Lambda, and ECS.

28. **Scenario: User reports “Access Denied” while uploading to S3. What could be the cause?**  
    Missing write permission in the policy or explicit deny.

29. **Can IAM policies be edited after attachment?**  
    Yes, for managed policies; inline policies can be updated per identity.

30. **Scenario: You want all users to follow MFA login. How do you enforce it?**  
    Use an IAM policy requiring MFA for all actions.

## Hard Level

31. **Scenario: You need to audit IAM user activity across AWS services. How do you do it?**  
    Enable AWS CloudTrail to log all user actions.

32. **What is the difference between resource-based and identity-based policies?**  
    Identity-based policies attach to users, groups, roles; resource-based policies attach to resources like S3 buckets.

33. **Scenario: How to restrict IAM users to access S3 only from specific IPs?**  
    Create a policy with `Condition` for `aws:SourceIp`.

34. **Scenario: How can you rotate IAM credentials securely?**  
    Use AWS Secrets Manager or rotate access keys manually.

35. **Scenario: How to provide programmatic access for an application to AWS?**  
    Create an IAM role with required permissions and use temporary credentials.

36. **Can IAM roles have trust policies?**  
    Yes, they define which entities can assume the role.

37. **Scenario: How to prevent an IAM user from deleting critical S3 buckets?**  
    Attach a policy with explicit `Deny` for delete actions.

38. **Scenario: You need cross-region access to resources for a Lambda function. How?**  
    Assign a role with required permissions and configure Lambda to assume it.

39. **Scenario: How do you enforce least privilege for developers?**  
    Grant only necessary permissions for tasks, monitor and adjust policies.

40. **Scenario: How to allow EC2 instances in different VPCs to access S3 securely?**  
    Attach IAM roles to instances and ensure proper VPC endpoint or policy permissions.

41. **Scenario: You need temporary access to AWS CLI for a contractor. How do you provide it?**  
    Create a role, generate temporary credentials, and provide them for the needed duration.

42. **Can an IAM user have both MFA and access keys?**  
    Yes, MFA is for console login; access keys are for programmatic access.

43. **Scenario: How do you audit IAM role assumption by EC2 instances?**  
    Use AWS CloudTrail to monitor `AssumeRole` API calls.

44. **Scenario: How to ensure no IAM user can create admin users?**  
    Apply policies that explicitly deny `iam:CreateUser` and admin permissions.

45. **Scenario: How do you prevent privilege escalation using IAM roles?**  
    Restrict `iam:PassRole` and `sts:AssumeRole` actions appropriately.

46. **Scenario: How to provide MFA-protected API access?**  
    Use IAM policy conditions that require MFA for API calls.

47. **Scenario: You need fine-grained access to a single S3 object. How?**  
    Attach an identity-based or resource-based policy allowing only that object.

48. **Scenario: How to enforce password rotation for IAM users?**  
    Use AWS account password policy settings.

49. **Scenario: You want to centralize IAM management across multiple accounts. How?**  
    Use AWS Organizations with service control policies (SCPs).

50. **Scenario: How to remove unused IAM users and clean up permissions?**  
    Audit via IAM reports, delete inactive users, and remove orphaned policies.
