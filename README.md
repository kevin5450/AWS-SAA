# AWS-SAA

AWS Certified Solutions Architect – Associate(SAA-C03) 학습 내용을 한곳에서 관리하기 위한 저장소입니다.

<p align="center">
  <a href="https://www.credly.com/badges/4a1cc8ec-283b-415a-a5dd-19e48a6378ea/public_url">
    <img src="assets/aws-saa-badge.png" alt="AWS Certified Solutions Architect - Associate" width="180" />
  </a>
</p>

<p align="center">
  <strong>AWS Certified Solutions Architect – Associate</strong><br/>
  SAA-C03 · Active · Valid through 2029-09-21
</p>

<p align="center">
  <a href="https://www.credly.com/badges/4a1cc8ec-283b-415a-a5dd-19e48a6378ea/public_url">Verify on Credly</a>
</p>

> GitHub README에서는 Credly의 `<script>` 임베드가 실행되지 않기 때문에 위에는 실제 AWS SAA 배지 이미지를 사용합니다.  
> 배지를 클릭하면 Credly 검증 페이지로 이동합니다. 실제 Credly embed 코드는 `docs/index.html`에 유지합니다.

---

## Repository Map

```text
AWS-SAA/
├─ README.md
├─ assets/
│  └─ aws-saa-badge.png    # AWS SAA 배지 이미지
├─ certifications/        # 자격증/배지 정보
├─ notes/                 # SAA 개념 정리
├─ labs/                  # AWS 실습
│  ├─ vpc-3tier/
│  ├─ ecs-cats-dogs/
│  └─ client-vpn/
├─ troubleshooting/       # 실습 중 오류와 해결 과정
├─ exam-review/           # 오답노트·키워드·복습
├─ study-log/             # 날짜별 학습 기록
├─ extras/
│  └─ agentic-ai/         # SAA 범위를 넘어선 AWS/AI 학습
└─ docs/
   └─ index.html           # GitHub Pages + Credly 실배지
```

## Core Notes

| 영역 | 문서 |
|---|---|
| VPC / Networking | [01-vpc-networking.md](notes/01-vpc-networking.md) |
| EC2 / ELB / ASG | [02-ec2-elb-asg.md](notes/02-ec2-elb-asg.md) |
| S3 / Storage | [03-s3-storage.md](notes/03-s3-storage.md) |
| Database | [04-databases.md](notes/04-databases.md) |
| IAM / KMS / WAF | [05-security-iam-kms-waf.md](notes/05-security-iam-kms-waf.md) |
| Lambda / SQS / SNS / EventBridge | [06-serverless-integration.md](notes/06-serverless-integration.md) |
| ECS / ECR / Containers | [07-containers-ecs-ecr.md](notes/07-containers-ecs-ecr.md) |
| CloudWatch / Config / Governance | [08-monitoring-governance.md](notes/08-monitoring-governance.md) |
| VPN / Direct Connect / TGW | [09-hybrid-networking.md](notes/09-hybrid-networking.md) |

## Labs

### VPC 3-Tier
VPC `10.0.0.0/16`, Public Subnet ×2, Private Subnet ×2, IGW, NAT Gateway, Public ALB, Private EC2를 직접 구성한 실습 기록입니다.

→ [labs/vpc-3tier](labs/vpc-3tier/README.md)

### ECS Cats & Dogs
ECR 이미지 → ECS Task Definition → ECS Service → ALB 연결 흐름을 정리합니다.

→ [labs/ecs-cats-dogs](labs/ecs-cats-dogs/README.md)

### Client VPN
Client VPN 구성과 접속 흐름을 별도 실습으로 관리합니다.

→ [labs/client-vpn](labs/client-vpn/README.md)

## Exam Review

문제 자체를 단순 암기하는 대신 다음 형식으로 누적합니다.

```text
문제의 힌트
→ 어떤 AWS 서비스가 답인지
→ 왜 정답인지
→ 다른 선지는 언제 정답이 되는지
```

- [Quick Keywords](exam-review/quick-keywords.md)
- [Wrong Answers](exam-review/wrong-answers.md)

## Study Rule

새로 공부한 내용은 아래 기준으로 저장합니다.

1. 개념이면 `notes/`
2. 직접 AWS에서 실행했으면 `labs/`
3. 오류가 발생했으면 `troubleshooting/`
4. 문제풀이에서 헷갈렸으면 `exam-review/`
5. 날짜별 진행 상황은 `study-log/`
6. SAA 범위를 넘어서는 AI/Agentic AI 내용은 `extras/`

## GitHub Pages

`docs/index.html`에는 Credly 공식 embed 코드가 포함되어 있습니다.

GitHub에서:

`Settings → Pages → Deploy from a branch → main /docs`

로 설정하면 저장소의 인증 페이지에서 실제 Credly 배지를 렌더링할 수 있습니다.
