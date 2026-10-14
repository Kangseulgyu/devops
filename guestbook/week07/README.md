# DevOps 7주차 - Docker Compose 실습 과제

## 1. `docker compose ps` 결과 (healthy 포함)
```text
NAME                IMAGE           COMMAND                  SERVICE   CREATED          STATUS
guestbook-nginx-1   nginx:alpine    "/docker-entrypoint.…"   nginx     21 minutes ago   Up 21 minutes
guestbook-redis-1   redis:7-alpine  "docker-entrypoint.s…"   redis     22 minutes ago   Up 21 minutes
guestbook-web-1     guestbook-web   "python app.py"          web       22 minutes ago   Up 21 minutes (healthy)
