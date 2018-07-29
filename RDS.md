# RDS

## Multi-AZ deployments for DB engines utilize synchronous physical replication to keep data on the standby up-to-date with the primary
  - MySQL
  - Oracle
  - MariaDB

## Read Replicas
  https://aws.amazon.com/rds/details/read-replicas/

  - 읽기 전용 복제본
  - enhanced performance
  - durability
  - 대표 데이터베이스
    + MySQL
    + MariaDB
    + PostgreSQL
    + Amazon Aurora

  단일 DB 인스턴스 용량 한도 이상으로 탄력적으로 확장하여 읽기 중심의 데이터베이스 워크로드를 쉽게 처리
  대량의 애플리케이션 읽기 트래픽 처리 가능

### Read Scaling
![Alt text](./images/read_scaling.jpg "read scaling")
