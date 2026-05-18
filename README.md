# ticketing-system

티켓팅 프로젝트의 전체 시스템 구성과 로컬 인프라 실행 환경을 관리하는 레포지토리입니다.

## 서비스 레포지토리

| 서비스 | Repository |
|---|---|
| User Service | [user-service](https://github.com/3s-ticketing/user-service) |
| Match Service | [match-service](https://github.com/3s-ticketing/match-service) |
| Seat Service | [seat-service](https://github.com/3s-ticketing/seat-service) |
| Reservation Service | [reservation-service](https://github.com/3s-ticketing/reservation-service) |
| Payment Service | [payment-service](https://github.com/3s-ticketing/payment-service) |
| Queue Service | [queue-service](https://github.com/3s-ticketing/queue-service) |
| Club Service | [club-service](https://github.com/3s-ticketing/club-service) |
| Common Module | [common-module](https://github.com/3s-ticketing/common-module) |
| Gateway Service | [gateway-service](https://github.com/3s-ticketing/gateway-service) |
| Config Server | [config-server](https://github.com/3s-ticketing/config-server) |
| Eureka Server | [eureka-server](https://github.com/3s-ticketing/eureka-server) |

## 로컬 인프라 실행

프로젝트 루트 경로에서 아래 명령어를 실행합니다.

```powershell
docker compose up -d
```

실행 상태 확인:

```powershell
docker compose ps
```

정상 실행되면 아래 컨테이너들이 `Up` 또는 `healthy` 상태로 보여야 합니다.

```text
ticketing-postgres
ticketing-redis
ticketing-kafka
ticketing-keycloak
```

컨테이너 종료:

```powershell
docker compose down
```

컨테이너와 볼륨 데이터까지 모두 삭제:

```powershell
docker compose down -v
```

주의: `docker compose down -v`를 실행하면 PostgreSQL, Redis, Kafka, Keycloak 데이터가 모두 삭제됩니다.