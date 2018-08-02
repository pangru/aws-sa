# VPC-Peering

## Invalid Peering Configuration

### Overlapping CIDR Block
- IPv4 CIDR 블록이 있는 vpc 간에는 VPC Peering

![](https://docs.aws.amazon.com/ko_kr/AmazonVPC/latest/PeeringGuide/images/overlapping-cidrs-diagram.png "")
![](https://docs.aws.amazon.com/ko_kr/AmazonVPC/latest/PeeringGuide/images/overlapping-multiple-cidrs-diagram.png "")

- IPv6 통신
![](https://docs.aws.amazon.com/ko_kr/AmazonVPC/latest/PeeringGuide/images/overlapping-cidrs-ipv6-diagram.png "")

### Transitive Peering
VPC A를 통해 VPC B에서 VPC C로 직접 패킷을 라우팅할 수 없습니다
![](https://docs.aws.amazon.com/ko_kr/AmazonVPC/latest/PeeringGuide/images/transitive-peering-diagram.png "")

### Edge to Edge routing via a gateway
- VPN 연결 또는 AWS Direct Connect 연결
![](https://docs.aws.amazon.com/ko_kr/AmazonVPC/latest/PeeringGuide/images/edge-to-edge-vpn-diagram.png "")

- Edge to Edge routing via Internet Gateway
인터넷에서의 트래픽은 VPC A에 대한 인터넷 게이트웨이 연결을 사용하여 VPC B에 직접 액세스할 수 없습니다.
![](https://docs.aws.amazon.com/ko_kr/AmazonVPC/latest/PeeringGuide/images/edge-to-edge-igw-diagram.png "")
