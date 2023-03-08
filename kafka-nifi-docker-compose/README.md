
Start the environment with `docker-compose up`. Once all services are up and running, there will be available several ports:

### Port 9092 - Kafka

Use this port to connect Kafka Producers, Kafka Consumers and other services directly communicating with Kafka.

+ Protocol: PLAINTEXT
+ Authentication: None

### Port 8082 - Kafka REST

REST interface to Kafka. 

Documentation for Kafka REST API: https://docs.confluent.io/current/kafka-rest/api.html

http://localhost:8082/v3/clusters

+ Protocol: HTTP
+ Authentication: None


### Port 8085 - Schema Registry

REST interface to Schema Registry.

+ Protocol: HTTP
+ Authentication: None

### Port 8080 - NiFi

NiFi user interface.

http://localhost:8080/nifi 

+ Protocol: HTTP
+ Authentication: None
