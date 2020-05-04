## Dependency for pom.xml

```
<dependency>
   <groupId>org.springframework.kafka</groupId>
   <artifactId>spring-kafka</artifactId>
</dependency>
<dependency>
   <groupId>org.springframework.kafka</groupId>
   <artifactId>spring-kafka-test</artifactId>
   <scope>test</scope>
 </dependency>
```

## Properties for application-dev.yml

```
spring:
    kafka:
        consumer:
          bootstrap-servers: localhost:9092
          group-id: group_id
          auto-offset-reset: earliest
          key-deserializer: org.apache.kafka.common.serialization.StringDeserializer
          value-deserializer: org.apache.kafka.common.serialization.StringDeserializer
        producer:
          bootstrap-servers: localhost:9092
          key-serializer: org.apache.kafka.common.serialization.StringSerializer
          value-serializer: org.apache.kafka.common.serialization.StringSerializer
```

## Run docker

```
docker-compose up -d
```

## Verify docker container

```
docker container ls
```
