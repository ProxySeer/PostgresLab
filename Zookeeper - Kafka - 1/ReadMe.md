**Download Link**  <br />

https://drive.google.com/drive/folders/1ulFCg-XJq9BksXLtHaJK9JeiJr_DJ0h-?usp=drive_link

**After the virtual machine starts, please follow the steps below.**
**The Zookeeper and Kafka services run automatically.**
**Run the following command to start the Debezium connector and sink connector to MongDb**
```ruby
sudo -i
/opt/kafka_2.13-3.8.0/bin/connect-standalone.sh /opt/kafka_2.13-3.8.0/config/connect-standalone.properties /opt/kafka_2.13-3.8.0/config/connect-mongo.properties /opt/kafka_2.13-3.8.0/config/connect-debezium-postgres.properties
```
