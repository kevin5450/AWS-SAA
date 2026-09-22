# Serverless / Integration

## Lambda
이벤트 기반 서버리스 컴퓨팅.

## SQS
서비스 간 비동기 Decoupling.
- Standard: 높은 처리량, 순서 보장 X
- FIFO: 순서/중복 제어가 중요할 때

## SNS
Pub/Sub 기반 Fan-out.

## EventBridge
이벤트 버스 기반 이벤트 라우팅. SaaS/AWS 서비스/커스텀 이벤트 연결에 적합.

## API Gateway
HTTP/REST/WebSocket API의 관리형 진입점.

## Step Functions
여러 서비스와 Lambda를 상태 기반 워크플로로 오케스트레이션.
