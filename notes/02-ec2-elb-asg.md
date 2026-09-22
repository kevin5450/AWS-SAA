# EC2 / ELB / Auto Scaling

## EC2
- AMI: 인스턴스를 시작하기 위한 이미지/부팅 템플릿
- EBS: 네트워크 기반 영구 블록 스토리지
- Instance Store: 호스트에 직접 연결된 임시 스토리지

## Lifecycle
- Reboot: 동일 호스트에서 OS 재부팅 성격
- Stop/Start: 재배치될 수 있으며 Public IPv4가 변경될 수 있음
- Terminate: 인스턴스 종료

## ELB
- ALB: Layer 7, HTTP/HTTPS, Host/Path 기반 라우팅
- NLB: Layer 4, TCP/UDP/TLS, 고성능·고정 IP 요구
- GWLB: 가상 보안 어플라이언스 통합

## Auto Scaling
수요에 따라 인스턴스 수를 조정하여 가용성과 비용 효율을 확보합니다.

## Purchase Options
- On-Demand: 약정 없이 유연
- Savings Plans: 사용량 약정 기반 할인, RI보다 유연한 범위 존재
- Reserved Instances: 특정 조건의 EC2 사용에 할인
- Spot: 중단 가능한 워크로드에 큰 할인
- Dedicated Host: 물리 서버 단위 제어/라이선스 요구
