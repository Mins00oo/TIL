## Redis를 시작하기 위한 내용을 간략하게 설명한 포스팅입니다.
---

### Redis 설치 (Docker)

```yml
version: '3.7'
services:
    redis:
        image: redis:6.2
        command: redis-server --requirepass 1234 --port 6379
        restart: always
        ports:
            - 6379:6379
```
`docker-compose up -d`
