# Routing

## Notfice
** In order to be routable to internet, we must add 0.0.0.0/0 (internet) as the destination and target (interget gateway)**

## Interget Gateway
## NAT device
  - for instances in private subnet
  
## Virtual Private Gateway
## VPC Peering Connection
  - 두 VPC 간에 트래픽을 라우틱할 수 있게 해주는 두 VPC 사이의 네트워킹 연결
  - https://docs.aws.amazon.com/ko_kr/AmazonVPC/latest/UserGuide/vpc-peering.html

## ClassicLink
  - EC2-Classic 인스턴스를 VPC에 연결

## Egress-Only Internet Gateway
  - VPC endpoint 와 다른 AWS Service 사이에 프라이빗 연결 생성