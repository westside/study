## Elastic search, Logstash, Kibana with docker
### 왜?
* usage case : [nginx로그 분석용 - elk with redis](https://medium.com/chequer/elkr-elasticsearch-logstash-kibana-redis-%EB%A5%BC-%EC%9D%B4%EC%9A%A9%ED%95%9C-%EB%A1%9C%EA%B7%B8%EB%B6%84%EC%84%9D-%ED%99%98%EA%B2%BD-%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0-f3dd9dfae622)
* 나의 경우에는 다양한 어플리케이션의 에러 로그(안드로이드, 윈도우 앱, 서버)를 쉽게 쌓고 (Logstash), 어디서 문제가 생겼는지 쉽게 살펴보고 알람도 받아보기 위해서 (Kibana). 그리고 그 중심에는 Elastic Search가 있음

### 비슷한 다른 것들 
* Splunk, Flume with Hadoop family

### How to start - The docker-compose setting
* https://github.com/deviantony/docker-elk

### 삽질들 
* 처음 띄울 때 Kibana는 뜨는 데 2분정도 걸린다. 당황하지 말기
* logback setting

pom.xml

### Collecting log fron spring boot app to logstash pipeline
```xml
<dependency>
	<groupId>net.logstash.logback</groupId>
	<artifactId>logstash-logback-encoder</artifactId>
	<version>4.11</version>
</dependency>
```

logback-spring.xml

```xml
<appender name="stash" class="net.logstash.logback.appender.LogstashTcpSocketAppender">
	<destination>host:5000</destination>
	<encoder class="net.logstash.logback.encoder.LogstashEncoder" />
</appender>
```


### nori를 포함하여 올리기
* http://sooyeol86.blogspot.com/2019/12/elasticsearch-with-nori-feat-docker.html
* DEV Console: http://localhost:5601/app/dev_tools#/console
* 사용자 파일 생성 방법: 정치인 이름이나 고유 명사 http://sooyeol86.blogspot.com/2019/12/elasticsearch-nori.html
* 



