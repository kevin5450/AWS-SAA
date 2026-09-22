# S3 / Storage

## S3 핵심 키워드
- S3 Transfer Acceleration: 장거리 업로드 가속
- Multipart Upload: 큰 객체 업로드를 여러 파트로 병렬 처리
- Intelligent-Tiering: 접근 패턴을 예측하기 어려운 데이터
- Lifecycle: 저장 등급 전환 및 만료 자동화
- Object Lock: WORM 기반 삭제/변조 방지

## EFS vs FSx
- EFS: Linux용 관리형 NFS 공유 파일 시스템
- FSx: Windows/Lustre/NetApp/OpenZFS 등 특정 파일 시스템 요구

## Instance Store vs EBS
- Instance Store: 매우 빠른 임시 로컬 스토리지
- EBS: EC2와 분리된 영구 블록 스토리지
