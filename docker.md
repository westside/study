## docker compose
```
docker-compose up
docker-compose start
docker-compose stop
```


## quick 
* error 
```
ERROR: for nginx  No such image: sha256:f01ad174a05de6d4c88f3953502782cd43b51715b9817d252f2150d4520ee69d\
```

* fix (https://github.com/docker/compose/issues/1113)
```
docker-compose rm
docker-compose up
```

## setup references
* https://spring.io/guides/gs/spring-boot-docker/
* https://github.com/docker/compose
* https://github.com/bhagwat/springboot-nginx-redis-docker
* http://geekyplatypus.com/tag/docker-compose/
