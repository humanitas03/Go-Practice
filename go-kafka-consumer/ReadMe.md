
## Confluent-kafka-Go
https://github.com/confluentinc/confluent-kafka-go

## Kafka 컨테이너 띄우기
```bash
cd docker-kafka-single-node
docker-compose up -d
```

## docker kafka 컨테이너에서 bash 실행하기

* 터미널에서 아래 명령어 실행
```bash
docker ps
```

* ```confluentinc/cp-kafka:latest``` 이미지에 대한 Container ID값을 찾고 아래에 대입한다.
```bash
docker exec -it [container ID] /bin/bash
```


## Kafka 관련 커맨드
* Topic 조회
```bash
/usr/bin/kafka-topics --bootstrap-server localhost:9092 --list
```

* Topic Create (name = myTopic)
```bash
/usr/bin/kafka-topics --create --bootstrap-server localhost:9092 --topic myTopic --partitions 1 --replication-factor 1
```

* message Producing
```bash
/usr/bin/kafka-console-producer --topic myTopic --broker-list localhost:9092
> {"notification":"알림"}
```
