# Kafka consumer example

## Run

```shell
./kafka-consumer -brokers="192.168.4.100:39092" -topics="events1" -group="boberKurwa" -oldest="true"
```

## kcat 
```shell
kcat -b 192.168.4.100:39092 -C -t events1 -f 'Topic %t[%p], offset: %o, key: %k, payload: %S bytes: %s\n'
kcat -b 192.168.4.100:39092 -C -t events1 -f 'Headers: %h: Message value: %s\n'
```
## Links:
- [IBM/sarama/examples/consumergroup](https://github.com/IBM/sarama/blob/main/examples/consumergroup/README.md)
- [docker-compose.yml example](https://github.com/katyagorshkova/kafka-kraft/blob/main/docker-compose.yml)
- [kcat](https://github.com/edenhill/kcat)

