# Kafka commands

Make sure you are under this directory: **kafka\bin**

## Starting a Zookeeper.

    ./zookeeper-server-start.sh ../config/zookeeper.properties

## Starte the Kafak Server (Make sure your server Zookeeper is up and running)

    ./kafka-server-start ../config/server-0.properties
