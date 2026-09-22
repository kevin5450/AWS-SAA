# VPC 3-Tier Lab

## Architecture
- VPC: `10.0.0.0/16`
- Public Subnet ×2
- Private Subnet ×2
- Internet Gateway
- NAT Gateway in Public Subnet
- Public ALB
- Private EC2

## Traffic
```text
Internet
   ↓
  IGW
   ↓
Public ALB
   ↓
Private EC2

Private EC2 outbound
   ↓
NAT Gateway
   ↓
IGW
   ↓
Internet
```

## Checkpoints
- Public Subnet RT: `0.0.0.0/0 → IGW`
- Private Subnet RT: `0.0.0.0/0 → NAT GW`
- ALB SG에서 Listener 포트 허용
- EC2 SG는 가능하면 ALB SG를 Source로 허용
