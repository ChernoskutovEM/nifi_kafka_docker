# nifi_kafka_docker

ETL example how to use nifi kafka zoo into docker compose 

####  How to up containers:

1. install docker in your OS
2. `cd ./kafka-nifi-docker-compose`
3. `sudo docker compose up`

#### Next nifi
1. open nifi http://localhost:8080/nifi 
2. load template from `./ETL-template-for-nifi` to NiFi with web ui
3. start nifi consumerKafka processors 

#### Next kafka
1. create topic
<pre><code>sudo docker exec -i kafka kafka-topics --create --topic nifi-test --topic-id id-1 --partitions 1 --replication-factor 1 --bootstrap-server localhost:9092
</code></pre>
2. check created topic 
<pre><code>sudo docker exec -i kafka kafka-topics --describe --topic nifi-test --exclude-internal --bootstrap-server localhost:9092</code></pre>
3. write to topic with cl
<pre><code>sudo docker exec -i kafka kafka-console-producer --topic nifi-test --bootstrap-server localhost:9092
a1
a2
a3 </code></pre>


#### Next nifi
1. check Queued into nifi web ui
2. done