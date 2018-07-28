## Configuring DNS Failover (Route 53 & Configure failover rhe S3 with CloudFront distribution)

posting a big article on the front page of website.
in the event of a load failure, set up DNS failover to a static website.

--> Use Route 53 and the failover option to failover to a static S3 website bucket or CloudFront distribution in the event of an issue.

https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover.html
https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover-configuring.html

-
# CloudFront
.html, .css, .js 및 이미지 파일과 같은 정적 및 동적 웹 컨텐츠를 사용자에게 더 빨리 배포하도록 지원하는 웹 서비스

- 컨텐츠가 이미 지연시간이 가장 낮은 엣지 로케이션에 있는 경우 CloudFront가 컨텐츠를 즉시 제공합니다
- 컨텐츠가 엣지에 없는 경우 CloudFront는, 컨텐츠의 최종 버전에 대한 소스로 지정된 오리진(S3 Bucket, Elemental MediaPackage 채널, HTTP 서버)에서 컨텐를 검색

CloudFront는 AWS 백본 네트워크를 통해 콘텐츠를 가장 효과적으로 서비스할 수 있는 엣지로 각 사용자 요청을 라우팅하여 콘텐츠 배포 속도를 높입니다. 
일반적으로 CloudFront 엣지가 최종 사용자에게 가장 빨리 제공합니다. 
AWS 네트워크를 사용하면 사용자의 요청이 반드시 통과해야 하는 네트워크의 수가 줄어들어 성능이 향상됩니다. 
파일의 첫 바이트를 로드하는 데 걸리는 지연 시간이 줄어들고 데이터 전송 속도가 빨라집니다. 또한 파일(객체라고도 함)의 사본이 
전 세계 여러 엣지 로케이션에 유지(또는 캐시)되므로 안정성과 가용성이 향상됩니다.

# Route 53?
## 도메인 이름 등록
## 인터넷 트래픽을 도메인의 리소스로 라우팅 (DNs가 브라우저를 웹 사이트 또는 웹 애플리케이션에 연결하도록 도움)
## 리소스 상태 확인
 - 리소스를 사용할 수 없게 될 때 알림을 수신하고 비정상 리소스가 아닌 다른 곳으로 인터넷 트래픽을 라우팅할 수 있음
## 도메인의 인터넷 트래픽을 라우팅


