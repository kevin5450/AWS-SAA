# Hybrid Networking

## Site-to-Site VPN
- Customer Gateway(CGW)
- Virtual Private Gateway(VGW) 또는 Transit Gateway
- IPsec 기반
- 일반적으로 두 개의 VPN 터널 제공

## Client VPN
개별 사용자가 AWS VPC에 원격 접속할 때 사용.

## Direct Connect
온프레미스와 AWS 간 전용 네트워크 연결.

### Private VIF
`On-prem → DX → Private VIF → VGW → VPC`

### Direct Connect Gateway
여러 VPC/리전을 확장 연결할 수 있는 연결 허브 역할.
DXGW 자체가 애플리케이션 로드밸런서를 제공하는 것은 아닙니다.

### Transit VIF
`On-prem → DX → Transit VIF → DXGW → TGW → Multiple VPCs`
