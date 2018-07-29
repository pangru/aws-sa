# Troubleshooting
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Troubleshooting.html

## Cannot connect to Amazon RDS DB Instance
    1. The local firewall is stopping the communication traffic
    2. The port cannot be used to send or receive communication for inbound and outbound
    3. The security groups for the DB are not properly configured
    4. DB instance is still being created and is not yet available.

## EC2
### In particular region, the Best recovery solution about Disaster
---
  Create an AMI of the EC2 Instance and copy it to another region


### 인터넷 연결이 안됩니다!
---
  https://aws.amazon.com/ko/premiumsupport/knowledge-center/elb-connectivity-troubleshooting/
  https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Scenario1.html
  
  1. VPC has an interget gateway attached
  2. Route table properly configured for the subnet
  3. A public IP or elastic IP address attached to the instance
  4. A route entry to the Internet gateway in the Route table
