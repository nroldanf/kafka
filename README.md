# Kafka

## Configuration with docker

```
docker-compose up -d
```

### Create a kafka topic
```
docker exec broker kafka-topics --bootstrap-server broker:9092 --create --topic quickstart
```

### List topics
```
docker exec broker kafka-topics --
```

### Send message to a topic
```
docker exec --interactive --tty broker kafka-console-producer --bootstrap-server broker:9092 --topic quickstart
```

### Read messages from a topic
```
docker exec --interactive --tty broker kafka-console-consumer --bootstrap-server broker:9092 --topic quickstart --from-beginning
```

## Resources

- https://developer.confluent.io/quickstart/kafka-docker/