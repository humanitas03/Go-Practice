
## Confluent-kafka-Go
https://github.com/confluentinc/confluent-kafka-go

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
