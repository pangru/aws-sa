# SNS (Simple Nortification Service)

## available endpoints
1) HTTP, HTTPS
2) Email, Email-JSON
3) SQS (FIFO queues are not currently supported)
4) SMS (phone number)

## what?
1) 게시-구독(pub-sub) 메세징 패러다임을 따름
2) 종량 과금제 청구

## what pro?
- 즉시적인 푸시 기반 전송
- 간편한 API와 손쉬운 애플케이션 통합
- 여러 전송 프로토콜을 지원하는 유연한 메세지 전송
- 사전 확약금 없는 저렴한 종량 과금제 모델
- 웹 기반 AWS Management Console의 간편한 포인트 앤 클릭 방식 인터페이스

## how logs?
SNS는 현재 인증된 호출에 대해서만 CloudTrail 감사를 지원. 
인증되지 않은 ConfirmSubscription 및 Unsubscribe 호출에 대한 CloudTrail Audit 로그는 사용 불가

# CloudTrail
AWS API 호출을 기록하고 로그 파일을 사용자에게 전달하는 웹 서비스