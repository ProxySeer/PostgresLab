**Download Link**  <br />

https://drive.google.com/drive/folders/1N_31nzU2HqlCTbY-5yDNYRqvMWlXqR48?usp=drive_link

**After the virtual machine starts, please follow the steps below.** <br />

**The Zookeeper and Kafka services run automatically.** <br />

**Run the following command to start the Debezium connector and sink connector to MongDb**
```ruby
sudo -i
/opt/kafka_2.13-3.8.0/bin/connect-standalone.sh /opt/kafka_2.13-3.8.0/config/connect-standalone.properties /opt/kafka_2.13-3.8.0/config/connect-mongo.properties /opt/kafka_2.13-3.8.0/config/connect-debezium-postgres.properties
```

**Run the following command to check if the consumer is running.**
```ruby
/opt/kafka_2.13-3.8.0/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test.numbers.publics.numbers --from-beginning
```
