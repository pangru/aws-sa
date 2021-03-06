# VPC (Virtual Private Cloud)
https://aws.amazon.com/ko/vpc/faqs/?nc1=h_ls

## 구성 요소
  1. Virtual Private Cloud : AWS 클라우드 내의 논리적으로 격리된 (isolated) 가상 네트워크
  2. Subnet : 격리된 리소스 그룹을 배치할 수 있는 VPC IP 주소 범위의 세그먼트
  3. Internet Gateway : 인터넷에 연결되는 VPC Gateway
  4. NAT Gateway : Private subnet에 있는 리소스가 인터넷에 액세스할 수 있도록 해주는 NAT 서비스 (Network Address Translation) 
  5. Hardware VPN Connection
  6. Virtual Private Gateway : VPN에 연결
  7. Customer Gateway
  7. Peering Connection : route traffic via private IP addresses between two peered VPCs
  8. VPC Endpoints
  9. Egress-only Internet Gateway

## Exams
#### #1. DNS hostname options of the VPC
![](./images/vpn-dns-hostname.jpeg)



#### #2. When you create a VPC using VPC wizard, an IGW is automatically created and associated with the VPC
  - https://docs.aws.amazon.com/ko_kr/AmazonVPC/latest/UserGuide/VPC_Internet_Gateway.html

## NAT Instances
Must be provisioned into a public subnet, and it must part of the private subnet's route table

## Establish the VPN connection
Must create a customer gateway resource in AWS <br/>

### the information to create a customer gateway resources
https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_VPN.html

![Alt text](./images/customer-gateway.jpeg "customer gateway information")

## [Security](Security.md)

## 유형
### Default VPCs
  - a logically isolated virtual network
  - automatically created for your AWS Account the first time you provision Aamazon EC2 resources

## Hosting a set of web and database servers
1. The web servers in a public subnet.
   The users can then access the application or web url via the Internet gateway to the web server.
2. The database servers in a private subnet. The database servers don't need to be accessed by the end users.

![Alt text](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/images/nat-gateway-diagram.png "nat gateway diagram")
https://docs.aws.amazon.com/ko_kr/AmazonVPC/latest/UserGuide/VPC_Subnets.html

## In order for the EC2 or ELBs to be accessible from internet
  - configure the route table for public subnet to route traffic to VPC internet gateway
    + https://docs.aws.amazon.com/ko_kr/AmazonVPC/latest/UserGuide/VPC_Route_Tables.html
    + Route table: 네트워크 트래픽을 전달할 위치를 결정하는데 사용되는 라우팅 규칙 포함
    
  - Add a rule on the instance's security group to allow traffic from the ELB's Security Group
  
  ![Alt text](./images/custom-route-table-diagram.png "route table diagram")
  

## Flow Logs
enable to capture information about the IP traffic going to and from network interfaces

https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/flow-logs.html
