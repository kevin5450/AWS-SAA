# Containers: ECR / ECS / EKS

## ECR
컨테이너 이미지를 저장하는 관리형 Registry.

## ECS
AWS의 컨테이너 오케스트레이션 서비스.

흐름:
`Docker Image → ECR → ECS Task Definition → ECS Service → ALB`

## Fargate
EC2 인스턴스를 직접 관리하지 않고 컨테이너 단위로 실행하는 서버리스 컴퓨트 옵션.

## EKS
관리형 Kubernetes.
