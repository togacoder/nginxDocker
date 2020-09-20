# README

## コマンド

```
 build . -t nginx
docker run -p 80:80 d --privileged -it [IMAGE ID] /sbin/init
docker exec -it [CONTAINER ID] /bin/bash
```

```
docker-compose build
docker-compose up -d
docker-compose exec --user user app /bin/bash
```