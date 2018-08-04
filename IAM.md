# IAM (Identity and Access Management)
https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html

Helps securely control access to AWS resources.


## AWS Root user
## User
  - an entity created in AWS
  - represents the person or service who uses the IAM user
  
## Group
  - collection of IAM users

## Role
  - similar to a user
  - idenity with permission policies

https://docs.aws.amazon.com/ko_kr/IAM/latest/UserGuide/id.html
https://docs.aws.amazon.com/ko_kr/IAM/latest/UserGuide/id_users.html

## IAM Roles for EC2
### Where should store API credentials whilst maintaining the maximum level security
  - Delegate permission to make API requests using IAM roles

## Identity Federation
https://aws.amazon.com/blogs/aws/aws-identity-and-access-management-now-with-identity-federation/

Existing identities (e.g. users) in your enterprise to access AWS APIs and resources using IAM's fine-graned access controls, without the need to create an IAM user for each identify.

- ~request temporary security credentials~ : short lived (1~36 hour) access keys, session tokens associated with the keys.

### How it Works
![](https://media.amazonwebservices.com/blog/iam_identity_federation_flow_4.png "")
