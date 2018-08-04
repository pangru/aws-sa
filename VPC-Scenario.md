# VPC-Scenario

## Scenario 1: VPC with a Single Public Subnet
- 블로그나 간단한 웹사이트 같은 단일 피어의 퍼블릭 웹 애플리케이션 실행해야 하는 경우
- 구성
  + IPV4 CIDR 블록의 크기가 /16(10.0.0.0/16)인 VPC, 65,536개의 private IPv4 주소 제공
  + CIDR 블록의 크기가 /24(10.0.0.0/24)인 서브넷, 256개의 private IPv4 주소 제공
  + Internet Gateway
  + private IPv4 address, public IPv4 address (Elastic IPv4 address)가 있는 인스턴스
  + custom route table associated with the subnet

![](https://docs.aws.amazon.com/ko_kr/AmazonVPC/latest/UserGuide/images/Case1_Diagram.png "")

## Scenario 2: VPC (NAT) with public subnet and private subnet
- 백엔스 서버에 대한 공개적인 액세스를 차단하고, public web application을 실행하려는 경우
- 예: 웹서버는 퍼블릿 서브넷, 데이터베이스 서버는 프라이빗 서브넷에 두는 다중 계층 웹사이트
- 구성
  + IPV4 CIDR 블록의 크기가 /16(10.0.0.0/16)인 VPC, 65,536개의 private IPv4 주소 제공
  + CIDR 블록의 크기가 /24(10.0.0.0/24)인 public subnet, 256개의 private IPv4 주소 제공
      * Internet Gateway로 이어지는 경로가 있는 route table과 연결됨
  + CIDR 블록의 크기가 /24(10.0.0.0/24)인 private subnet, 256개의 private IPv4 주소 제공
  + Internet Gateway
  + Instances with private IPv4 address. 
  + Instances with public subnet with Elastic IPv4 address
  + NAT Gateway with own Elastic IPv4 address (private IP를 가진 인스턴스의 요청을 외부로 보낼 수 있도록 도와줌)
  + custom route table associated with the public subnet
  + main route table associated the public subnet (다른 vpc내 인스턴스와 통신할 수 있도록 도와줌)

![](https://docs.aws.amazon.com/ko_kr/AmazonVPC/latest/UserGuide/images/nat-gateway-diagram.png "")

## Scenario 3: VPC with Public and Private Subnets and AWS Managed VPN Access
- 퍼블릭 서브넷과 프라이빗 서브넷이 있는 Virtual Private Cloud(VPC)와 IPsec VPN 터널을 통해 귀사의 네트워크와 통신하기 위한 가상 프라이빗 게이트웨이가 포함
- 네트워크를 클라우드로 확장하고, vpc로부터 직접 인터넷에 액세스 하려는 경우
- 구성
  + IPV4 CIDR 블록의 크기가 /16(10.0.0.0/16)인 VPC, 65,536개의 private IPv4 주소 제공
  + CIDR 블록의 크기가 /24(10.0.0.0/24)인 public subnet, 256개의 private IPv4 주소 제공
      * Internet Gateway로 이어지는 경로가 있는 route table과 연결됨
  + CIDR 블록의 크기가 /24(10.0.0.0/24)인 private subnet, 256개의 private IPv4 주소 제공
  + Internet Gateway
  + VPC와 Network 사이의 VPN 연결
      * AWS Virtual Private Gateway와 VPN 연결 사용자의 Custom Gateway로 구성
  + Instance with private IPv4 address
  + Instance with public IPv4 address (Elastic IPv4 address)가 있는 인스턴스
  + custom route table associated with the public subnet
  + main route table associated with VPN-only subnet

![](https://docs.aws.amazon.com/ko_kr/AmazonVPC/latest/UserGuide/images/Case3_Diagram.png "")

## Scenario 4: VPC with a Private Subnet Only and AWS Managed VPN Access
- 네트워크를 인터넷에 노출하지 않고 Amazon 인프라를 사용하여 네트워크를 클라우드로 확장하려는 경우
- VPC + IPsec VPN Tunnel
- 구성
  + IPV4 CIDR 블록의 크기가 /16(10.0.0.0/16)인 VPC, 65,536개의 private IPv4 주소 제공
  + CIDR 블록의 크기가 /24(10.0.0.0/24)인 private subnet, 256개의 private IPv4 주소 제공
  + VPN 연결 : Virtual Private Gateway <-- VPN --> Cutomer Gateway
  + Instances with private IPv4 address. 
  + main route table associated the public subnet (다른 vpc 인스턴스와 통신할 수 있도록 도와줌)

![](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/images/Case4_Diagram.png "")

