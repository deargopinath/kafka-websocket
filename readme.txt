# Stream kafka messages over web socket

+-----------------------------+
|          Browser            |
+-------------+---------------+
              |
              ^
              |
+-------------+---------------+
|         Web Socket          |
+-------------+---------------+
              |   
              ^    
              |     
+-------------+---------------+
|         Kafka topic         |
+-----------------------------+



# Instructions to deploy and demonstrate

1. Install Kafka (https://www.confluent.io/download/) at C:\confluent41
2. Run `start-kafka.cmd` to start Kafka
3. Run `create-kafka-topic.bat` to create kafka topic
4. Build the project using mvn clean install
5. Run `java -jar target\kafka-writer.jar to send test data to kafka topic.
6. Run java -jar target\kafka-websocket.jar to start websocket service
7. Open http://localhost:8080 to see websocket data
