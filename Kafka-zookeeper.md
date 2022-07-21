# Zookeeper-Kafka Hands on commands

## Create a topic, lsit topics, describe a topic, and delete topic

	zookeeper-server-start config/zookeeper.properties # start zookeeper

### Kafka:

	kafka-server-start config/server.properties #start Kafka server

### Creating topic:

	Kafka-topics --create --topic <topic-name>  --partitions 3 --replication-factor 1 --zookeeper localhost:2181

	kafka-topics --create --topic first_topic --partitions 3 --replication-factor 1 --zookeeper localhost:2181

### List all the topics:

	kafka-topics --list -zookeeper localhost:2181

### Topic description:

	kafka-topics --topic <topic-name> --describe -zookeeper localhost:2181
	kafka-topics --topic first_topic --describe -zookeeper localhost:2181 

### Topic deletion:

	Kafka-topics —topic <topic-name> —delete -zookeeper localhost:2181 
	Kafka-topics —topic secound_topic —delete -zookeeper localhost:2181
	
### Kafka-console-producer
	
	kafka-console-producer --broker-list localhost:9092 --topic 2st_topic --producer-property acks=all

### Kafka-console-consumer
	
	kafka-console-consumer --bootstrap-server localhost:9092 --topic first-_topic
	
*To read message from beginning*

	kafka-console-consumer --bootstrap-server localhost:9092 --topic first-_topic --from-beginning

### Attaching consumer to a group
	
	kafka-console-consumer —bootstrap-server localhsost:9092 —topic 1st_topic — group my-frist-application  --from-beginning
