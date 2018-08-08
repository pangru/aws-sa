# Troubleshooting
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Troubleshooting.html

## Best Practice
https://d0.awsstatic.com/whitepapers/aws-web-hosting-best-practices.pdf

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


## IAM
### Best Practice
https://docs.aws.amazon.com/ko_kr/IAM/latest/UserGuide/best-practices.html
  - root 사용자 액세스키 잠그기
  - 개별 사용자 만들기
  - 그룹을 사용하여 IAM 사용자에게 권한 할당
  - 가급적 AWS 정의 정책을 이용해 권한 할당
  - 최소 권한 부여
  - 액세스 레벨을 이용한 권한 검토
  - 역할을 사용하여 위임
  
