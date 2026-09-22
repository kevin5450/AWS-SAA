# ECS Cats & Dogs Lab

## Goal
ECR에 저장한 컨테이너 이미지를 ECS에서 실행하고 ALB를 통해 접근합니다.

## Flow
```text
Source
 ↓
Docker Build
 ↓
ECR
 ↓
ECS Task Definition
 ↓
ECS Service
 ↓
ALB
 ↓
Client
```

## Notes
- ECR은 이미지를 저장하는 Registry.
- ECS는 ECR의 이미지를 Pull하여 Task를 실행.
- Task Execution Role은 ECS가 ECR 이미지 Pull, CloudWatch Logs 전송 등에 사용하는 권한과 관련됨.
- 서비스/Task 보안 그룹과 ALB 보안 그룹 관계를 명확히 기록할 것.

## Troubleshooting template
```text
Symptom:
Cause:
Check:
Fix:
Why it worked:
```
