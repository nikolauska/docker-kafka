# Kafka in Docker

This repository provides everything you need to run Kafka in Docker.

## Run

```bash
docker run -p 2181:2181 -p 9092:9092 --env ADVERTISED_HOST=`docker-machine ip \`docker-machine active\`` --env ADVERTISED_PORT=9092 nikolauska/kafka
```

```bash
export KAFKA=`docker-machine ip \`docker-machine active\``:9092
kafka-console-producer.sh --broker-list $KAFKA --topic test
```

```bash
export ZOOKEEPER=`docker-machine ip \`docker-machine active\``:2181
kafka-console-consumer.sh --zookeeper $ZOOKEEPER --topic test
```

## Public Builds

https://registry.hub.docker.com/u/nikolauska/kafka/

## Build from Source

```
docker build -t nikolauska/kafka .
```


