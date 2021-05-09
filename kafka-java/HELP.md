# Read Me First
The following was discovered as part of building this project:

* The original package name 'com.syntegrity.javakafka.kafka-java' is invalid and this project uses 'com.syntegrity.javakafka.kafkajava' instead.

# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/2.4.5/maven-plugin/reference/html/)
* [Create an OCI image](https://docs.spring.io/spring-boot/docs/2.4.5/maven-plugin/reference/html/#build-image)
* [Spring Web](https://docs.spring.io/spring-boot/docs/2.4.5/reference/htmlsingle/#boot-features-developing-web-applications)
* [Spring for Apache Kafka](https://docs.spring.io/spring-boot/docs/2.4.5/reference/htmlsingle/#boot-features-kafka)

### Guides
The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/bookmarks/)

### Start SpringBoot
Run Configuration
Goals - spring-boot:run

### Producer
http://localhost:8080/kafka/produce?message=This%20is%20my%20message4

### Consumer
http://localhost:8080/kafka/messages

### Start Zookeeper
zookeeper-server-start.sh config/zookeeper.properties

### Start Kafka
kafka-server-start.sh config/server.properties

### Create Topic
kafka-topics.sh --zookeeper 127.0.0.1:2181 --topic myTopic --create --partitions 3 --replication-factor 1

### topic list 
kafka-topics.sh --zookeeper 127.0.0.1:2181 --list

### Create Consumer and read
kafka-consumer-groups.sh --bootstrap-server 127.0.0.1:9092 --group app1
kafka-console-consumer.sh --bootstrap-server 127.0.0.1:9092 --topic myTopic --group app3
kafka-console-consumer.sh --bootstrap-server 127.0.0.1:9092 --topic myTopic

### consumer describe
kafka-consumer-groups.sh --bootstrap-server 127.0.0.1:9092 --group app3 --describe

### Consumer reset
kafka-consumer-groups.sh --bootstrap-server 127.0.0.1:9092 --group app1 --reset-offsets --to-earliest --execute --topic first_topic


