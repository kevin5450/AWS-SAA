# AWS-SAA

SAA 공부하면서 정리했던 내용이랑 실습 기록을 모아두는 저장소입니다.

처음에는 시험 준비용으로 시작했는데, 공부하다 보니 VPC나 ECS처럼 직접 구성해본 내용이랑  
실습하면서 막혔던 부분도 같이 남겨두는 게 좋을 것 같아서 계속 추가하고 있습니다.

<p align="center">
  <a href="https://www.credly.com/badges/4a1cc8ec-283b-415a-a5dd-19e48a6378ea/public_url">
    <img src="assets/aws-saa-badge.png" alt="AWS Certified Solutions Architect - Associate" width="180" />
  </a>
</p>

<p align="center">
  AWS Certified Solutions Architect – Associate (SAA-C03)<br/>
  Valid through 2029-09-21
</p>

배지를 누르면 Credly 인증 페이지로 이동합니다.

---

## 정리해둔 내용

| 주제 | 정리 |
|---|---|
| VPC / Networking | [VPC, Subnet, Route Table, SG, NACL 등](notes/01-vpc-networking.md) |
| EC2 / ELB / ASG | [EC2, EBS, ALB/NLB/GWLB, Auto Scaling](notes/02-ec2-elb-asg.md) |
| S3 / Storage | [S3, EFS, FSx](notes/03-s3-storage.md) |
| Database | [RDS, Aurora, DynamoDB, ElastiCache, Redshift](notes/04-databases.md) |
| Security | [IAM, KMS, WAF](notes/05-security-iam-kms-waf.md) |
| Serverless | [Lambda, SQS, SNS, EventBridge](notes/06-serverless-integration.md) |
| Container | [ECR, ECS, EKS](notes/07-containers-ecs-ecr.md) |
| Monitoring | [CloudWatch, CloudTrail, Config](notes/08-monitoring-governance.md) |
| Hybrid | [VPN, Direct Connect, DXGW, TGW](notes/09-hybrid-networking.md) |

전체 흐름은 [roadmap](notes/00-roadmap.md)에 따로 정리했습니다.

## 실습

### VPC 3-Tier

회사 Sandbox에서 VPC부터 직접 만들면서 진행한 실습입니다.

`VPC → Public/Private Subnet → IGW/NAT → ALB → EC2`

라우팅 테이블이나 SG를 잘못 잡았을 때 어디부터 확인해야 하는지도 같이 기록하려고 합니다.

→ [VPC 3-Tier 실습](labs/vpc-3tier/README.md)

### ECS Cats & Dogs

ECR에 이미지를 올리고 ECS에서 Task/Service로 실행한 뒤 ALB까지 연결한 실습입니다.

`Docker Image → ECR → ECS → ALB`

Task Execution Role, Security Group, ECR Image URI처럼 실습하면서 헷갈렸던 부분도 같이 정리했습니다.

→ [ECS 실습](labs/ecs-cats-dogs/README.md)

### Client VPN

Client VPN은 별도로 구성해보면서 순서대로 기록할 예정입니다.

→ [Client VPN 실습](labs/client-vpn/README.md)

## 시험 준비할 때 헷갈렸던 것

문제를 많이 풀면서 반복해서 틀렸던 개념이나,  
문제에서 어떤 문장이 정답 힌트였는지를 따로 모으고 있습니다.

- [빠르게 보는 키워드](exam-review/quick-keywords.md)
- [오답 정리](exam-review/wrong-answers.md)

단순히 정답만 적기보다는

```text
문제에서 잡아야 하는 힌트
→ 왜 이 서비스가 답인지
→ 다른 선택지는 언제 답이 되는지
```

정도까지는 같이 적어두려고 합니다.

## 폴더

```text
AWS-SAA/
├─ assets/              # 이미지
├─ certifications/     # 자격증 관련
├─ notes/              # 개념 정리
├─ labs/               # 직접 해본 실습
├─ troubleshooting/    # 오류 / 해결 과정
├─ exam-review/        # 시험 복습, 오답
├─ study-log/          # 공부 기록
├─ extras/             # SAA 외에 추가로 공부한 내용
└─ docs/               # GitHub Pages
```

앞으로 AWS 공부나 실습하면서 새로 알게 된 내용은 계속 이 저장소에 추가할 예정입니다.
