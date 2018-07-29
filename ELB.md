# Elastic Load Balancer

https://aws.amazon.com/ko/elasticloadbalancing/

<b>To evenly distribute traffic among multiple EC2 instances in seperate Availability Zones</b>

  - the most the ideal solution for adding elasticity to an application

## Classic Load Balancer
- load balance HTPP/HTTPS applications
- strict layer 4 Load Balancing for applications that rely purely on the TCP protocoal,
- can define the Load Balancer protocol as TCP
- 여러 Amazon EC2 인스턴스에서 기본적인 로드 밸런싱을 제공
- EC2-Classic 네트워크 내에 구축된 애플리케이션용

## Application Load Balancer
- distribute HTTP/HTTPS traffic, depends on the TCP protocol.
- HTTP 및 HTTPS 트래픽의 로드 밸런싱에 가장 적합하며, 마이크로서비스와 컨테이너 등 최신 애플리케이션 아키텍처 전달을 위한 고급 요청 라우팅 기능 제공
- 개별 요청 수준(레이어 7)에서 작동
- 요청의 콘텐츠를 기반으로 Amazon Virtual Private Cloud(Amazon VPC) 내의 대상으로 트래픽을 라우팅

## Network Load Balancer
- 극한의 성능이 요구되는 TCP 트래픽의 로드 밸런싱에 가장 적합
- 연결 수준(레이어 4)에서 작동하는 Network Load Balancer는 Amazon Virtual Private Cloud(Amazon VPC) 내의 대상으로 트래픽을 라우팅
- 초당 수백만 개의 요청을 처리하면서 극히 낮은 지연 시간 유지 가능 
- 갑작스러운 일시적 트래픽 패턴 처리에도 최적화
