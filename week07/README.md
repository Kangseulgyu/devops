7주차 
1. docker compose ps 결과
userseul@BOOK-UHJSJLLDVL:~/devops/week07/guestbook$ docker compose ps
NAME                IMAGE            COMMAND                  SERVICE   CREATED              STATUS                        PORTS
guestbook-nginx-1   nginx:alpine     "/docker-entrypoint.…"   nginx     About a minute ago   Up About a minute             0.0.0.0:8080->80/tcp, [::]:8080->80/tcp
guestbook-redis-1   redis:7-alpine   "docker-entrypoint.s…"   redis     About a minute ago   Up About a minute (healthy)   6379/tcp
guestbook-web-1     guestbook-web    "python app.py"          web       About a minute ago   Up About a minute (healthy)   5000/tcp

2. ![scale 결과](./scale.png)

3. up: 컨테이너와 네트워크는 삭제되지만, 볼륨은 유지
up을 실행해도 기존에 저장되었던 데이터가 그대로 보존

 down: 컨테이너, 네트워크뿐만 아니라 볼륨까지 완전히 삭제됨

4. 비밀번호 인증 정보 유출 방지
공개 레포지토리 보안 사고 예방
환경별 독립성 유지
