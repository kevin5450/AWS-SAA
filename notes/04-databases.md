# Databases

## RDS / Aurora
관계형 데이터, SQL, 트랜잭션, 기존 MySQL/PostgreSQL 호환성이 핵심이면 우선 고려합니다.

- Multi-AZ: 고가용성/장애 조치
- Read Replica: 읽기 확장
- RDS Proxy: 다수의 짧은 DB 연결을 풀링하여 DB 연결 부하 완화

## DynamoDB
- 서버리스 NoSQL Key-Value/Document DB
- 매우 낮은 지연과 자동 확장
- DynamoDB Streams: 항목 변경 이벤트 처리

## ElastiCache
- Redis: 복잡한 자료구조, 복제, 영속성 등
- Memcached: 단순 분산 메모리 캐시

## Redshift
대규모 분석용 데이터 웨어하우스.

## Athena
S3 데이터를 서버리스 SQL로 즉석 분석할 때 강함.
