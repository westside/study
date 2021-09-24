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

```
PUT test2
{
  "settings": {
    "analysis": {
      "tokenizer": {
        "nori_user_dict": {
          "type": "nori_tokenizer",
          "decompound_mode": "mixed",
          "user_dictionary": "user_dic.txt"
        }
      },
      "analyzer": {
        "korean_analyzer": {
          "filter": [
            "pos_filter_speech", "nori_readingform",
            "lowercase", "synonym", "remove_duplicates"
          ],
          "tokenizer": "nori_user_dict"
        }
      },
      "filter": {
        "synonym" : {
          "type" : "synonym_graph",
          "synonyms_path" : "synonyms.txt"
        },
        "pos_filter_speech": {
          "type": "nori_part_of_speech",
          "stoptags": [
            "E", "J", "SC", "SE", "SF", "SP", "SSC", "SSO", "SY", "VCN", "VCP",
            "VSV", "VX", "XPN", "XSA", "XSN", "XSV"
          ]
        }
      }
    }
  }
}
```

* anaylize
```
POST test2/_analyze
{
    "analyzer":"korean_analyzer",
    "text":"북한은 삼성전자 24일 문재인 대통령이 유엔총회 연설에서 거듭 제의한 종전선언에 대해 시기상조라며, 미국의 적대시 정책이 남아있는 한 종전선언은 허상 이라는 제목의 담화를 발표했다.북한은 다만 담화를 시작하며 앞으로 평화보장체계 수립에로 나가는데서 종전을 선언하는 것은 한번은 짚고 넘어가야할 문제인 것만은 분명하다고 밝혀, 향후 논의의 여지는 남겼다. 리태성 북한 외무성 부상은 이날 북한의 대외매체인 조선중앙통신에 게재한 담화에서 눈앞의 현실은 종전선언 채택이 시기상조라는 문제를 제기하고 있다며, 올해 2월과 8월에 미 본토 캘리포니아 주 반덴버그공군기지에서 진행된 미니트맨-3 대륙간탄도미사일시험발사도, 5월에 전격 발표된 미국 남조선미사일지침종료 선언도, 일본과 남조선에 대한 수십억달러분의 무장장비판매승인도 모두 우리를 겨냥한 것이라는 것은 세상이 잘 알고 있다고 주장했다."
}
```
* add doc : https://www.elastic.co/guide/en/elasticsearch/reference/current/docs-index_.html
```
POST test2/_doc/
{
  "@timestamp": "2099-11-15T13:12:00",
  "message": "북한은 삼성전자 24일 문재인 대통령이 유엔총회 연설에서 거듭 제의한 종전선언에 대해 시기상조라며, 미국의 적대시 정책이 남아있는 한 종전선언은 허상 이라는 제목의 담화를 발표했다.북한은 다만 담화를 시작하며 앞으로 평화보장체계 수립에로 나가는데서 종전을 선언하는 것은 한번은 짚고 넘어가야할 문제인 것만은 분명하다고 밝혀, 향후 논의의 여지는 남겼다. 리태성 북한 외무성 부상은 이날 북한의 대외매체인 조선중앙통신에 게재한 담화에서 눈앞의 현실은 종전선언 채택이 시기상조라는 문제를 제기하고 있다며, 올해 2월과 8월에 미 본토 캘리포니아 주 반덴버그공군기지에서 진행된 미니트맨-3 대륙간탄도미사일시험발사도, 5월에 전격 발표된 미국 남조선미사일지침종료 선언도, 일본과 남조선에 대한 수십억달러분의 무장장비판매승인도 모두 우리를 겨냥한 것이라는 것은 세상이 잘 알고 있다고 주장했다.",
  "user": {
    "id": "안년"
  }
}
```


* search https://www.elastic.co/guide/en/elasticsearch/reference/current/search-search.html

```
GET /test2/_search
{
  "query": {
    "term": {
      "message": "문재인"
    }
  }
}
```



### 명령어
https://www.elastic.co/guide/en/elasticsearch/reference/current/docs-index_.html
```


```

