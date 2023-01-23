## Redis를 시작하기 위한 내용을 간략하게 설명한 포스팅입니다.
---

### Redis 설치 (Docker)

```yml
version: '3.7'

services:
    redis:
        container_name: redis-server
        image: redis:alpine
        command: redis-server --requirepass 1234 --port 6379
        hostname: redis-server
        restart: always
        ports:
          - 6379:6379
```
`docker-compose up -d`
