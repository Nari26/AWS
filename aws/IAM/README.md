# What is IAM
AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources. You use IAM to control who is authenticated (signed in) and authorized (has permissions) to use resources.

- AWS documentation https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html

# IAM features
- Shared access to your AWS account
- Granular permissions
- Secure access to AWS resources for applications that run on Amazon EC2
- Multi-factor authentication (MFA)
- Identity federation
- Identity information for assurance
- Integrated with many AWS services
- Eventually Consistent
- Free to use

# IAM Architecture
![alt text](https://github.com/Nari26/AWS/blob/master/aws/IAM/IAM_architecture.png)

## 1. IAM Users:
- An AWS IAM user is an entity that you create in AWS to represent the person or application that uses it to interact with AWS. A user in AWS consists of a name and credentials.
- Adding an IAM User - https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html#id_users_create_console

## 2. IAM user groups:
- An IAM user group is a collection of IAM users. User groups let you specify permissions for multiple users, which can make it easier to manage the permissions for those users.
- Adding an IAM user group - https://docs.aws.amazon.com/IAM/latest/UserGuide/id_groups_create.html
- Managing IAM user groups - https://docs.aws.amazon.com/IAM/latest/UserGuide/id_groups_manage.html

## 3. IAM Role: 
- An IAM role is similar to an IAM user, in that it is an AWS identity with permission policies that determine what the identity can and cannot do in AWS. However, instead of being uniquely associated with one person, a role is intended to be assumable by anyone who needs it. 
- Also, a role does not have standard long-term credentials such as a password or access keys associated with it. Instead, when you assume a role, it provides you with temporary security credentials for your role session.
- Creating an IAM Role - https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user.html#roles-creatingrole-user-console

## 4. IAM Policy:
- IAM gives you the tools to create and manage all types of IAM policies (managed policies and inline policies). 
- To add permissions to an IAM identity (IAM user, group, or role), you create a policy, validate the policy, and then attach the policy to the identity. You can attach multiple policies to an identity, and each policy can contain multiple permissions.
- Creating an IAM Policy - https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_create-console.html#access_policies_create-json-editor

