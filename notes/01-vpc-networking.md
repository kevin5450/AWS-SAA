# VPC / Networking

## CIDR
- RFC1918 대표 사설 대역
  - `10.0.0.0/8`
  - `172.16.0.0/12`
  - `192.168.0.0/16`
- VPC에는 Secondary CIDR 추가 가능.
- Subnet은 하나의 AZ에 속함.

## Public vs Private Subnet
- Public Subnet의 핵심: Route Table에 `0.0.0.0/0 → IGW` 경로 존재.
- Public IP만 있다고 Public Subnet이 되는 것은 아님.
- Private Subnet의 인터넷 Outbound는 일반적으로 NAT Gateway를 사용.

## Security Group vs NACL
| 구분 | Security Group | NACL |
|---|---|---|
| 적용 | ENI/리소스 | Subnet |
| 상태 | Stateful | Stateless |
| Rule | Allow only | Allow + Deny |
| 평가 | 전체 Rule | 낮은 번호부터 첫 일치 |

## Endpoint
- Gateway Endpoint: S3, DynamoDB
- Interface Endpoint: AWS PrivateLink 기반 다수 AWS 서비스
- 목적: 인터넷/NAT를 거치지 않고 AWS 서비스에 Private 접근

## Peering vs Transit Gateway
- VPC Peering: 1:1, 전이 라우팅 불가
- Transit Gateway: 여러 VPC/VPN 연결을 중앙 집중화

## Internet Gateway
IGW는 VPC와 인터넷 간 출입구입니다. 인터넷 통신을 위해서는 라우팅뿐 아니라 리소스의 Public IPv4/EIP 등도 함께 고려해야 합니다.
