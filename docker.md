## what is docker? and how?
* https://www.docker.com/what-docker
* 도커 무작정 따라하기 : https://www.slideshare.net/pyrasis/docker-fordummies-44424016
* Docker로 서버 개발 편하게 하기 https://www.slideshare.net/jhgod/docker-62527504

## docker in AWS 
* ECR : https://aws.amazon.com/ecr/
* ECS : https://aws.amazon.com/ecs/



## docker compose
```
docker-compose up
docker-compose start
docker-compose stop
```


## Tips

* error fix  (https://github.com/docker/compose/issues/1113)
```
ERROR: for nginx  No such image: sha256:f01ad174a05de6d4c88f3953502782cd43b51715b9817d252f2150d4520ee69d\
```

```
docker-compose rm
docker-compose up
```


## docker command

```
docker build -t tag-name .
docker run -p 80:80 -t tag-name
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```


## setup references
* https://spring.io/guides/gs/spring-boot-docker/
* https://github.com/docker/compose
* https://github.com/bhagwat/springboot-nginx-redis-docker
* http://geekyplatypus.com/tag/docker-compose/
