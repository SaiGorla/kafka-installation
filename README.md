# kafka-installation

## Kafka Commands:

 Open PowerShell in C:\kafka_2.13-2.7.0 folder.

Open the new window and Run Zookeeper Service  (keep window open)
```
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```
Use new window to the Run Kafka Service (keep window open)
```
.\bin\windows\kafka-server-start.bat .\config\server.properties
```
Use new window Execute One-Time Commands - create, list, delete topics 
```
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic bearcat-messages

.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list
```
Use new window Run Kafka Producer will provide a > prompt for writing messages
```
.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic bearcat-messages
```
Type your messages in this powershell window.

Now, use the new window Run Kafka Consumer is used to show all the previous written messages.
```
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic bearcat-messages --from-beginning
```
 All the information that you have given in the 4th command shows us in the powershell window.
