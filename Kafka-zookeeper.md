# Zookeeper-Kafka start and stop servers

## Create a topic, lsit topics, describe a topic, and delete topic

	zookeeper-server-start config/zookeeper.properties # start zookeeper

### Kafka:

	kafka-server-start config/server.properties #start Kafka server

### Creating topic:

	Kafka-topics --zookeeper localhost:2181 --topic <topic-name> --create --partitions 3 --replication-factor 1

	kafka-topics --zookeeper localhost:2181 --topic first_topic --create --partitions 3 --replication-factor 1

### List all the topics:

	kafka-topics -zookeeper localhost:2181 --list

### Topic description:

	kafka-topics -zookeeper localhost:2181 --topic <topic-name> --describe
	kafka-topics -zookeeper localhost:2181 --topic first_topic --describe

### Topic deletion:

	Kafka-topics -zookeeper localhost:2181 —topic <topic-name> —delete
	Kafka-topics -zookeeper localhost:2181 —topic secound_topic —delete
	
### Kafka-console-producer
	
	kafka-console-producer --broker-list localhost:9092 --topic 2st_topic --producer-property acks=all

### Kafka-console-consumer
	
	kafka-console-consumer --bootstrap-server localhost:9092 --topic first-_topic
	
*To read message from beginning*

	kafka-console-consumer --bootstrap-server localhost:9092 --topic first-_topic --from-beginning

### Attaching consumer to a group
	
	kafka-console-consumer —bootstrap-server localhsost:9092 —topic 1st_topic — group my-frist-application  --from-beginning
