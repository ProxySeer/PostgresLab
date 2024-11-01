# Project Overview

**!!! The architecture below is set up on virtual servers and ready to run. !!!**  
All virtual machines have their own download links available in the `README.md` file within their respective folders, and all commands to be executed after starting the virtual machines are also included.

**Please read the `README.md` file in each folder after starting the virtual machines.**  

**The entire structure below is designed to be suitable for HA/DR solutions on virtual machines. While doing these installations, I used a total of 17 virtual machines. The setup includes the following technologies. All server installations were performed on Ubuntu:**

- Multiple HAProxy  
- Multiple PgBouncer  
- PostgreSQL Cluster  
- Consul Cluster  
- Patroni  
- PgBackRest  
- PgWatch  
- PgBadger  
- Logical Replication  
- Debezium - Zookeeper - Kafka Cluster  
- MongoDB Cluster  

**The total size is around 400 GB. Each server has the same configuration, requiring a minimum of 17 GB RAM. Additionally, to ensure the structure works correctly, please watch the video (Starting up the servers) I’ve prepared before starting the servers; otherwise, they may not work. You need to follow the steps in the video in order. This setup will provide you with numerous opportunities for testing and learning —> [Click to add a new node to the cluster](https://github.com/ProxySeer/PostgresLab/blob/main/How%20to%20add%20a%20new%20node/ReadMe.md).**

## Order of Starting the Virtual Machines

1. Consul - 1  
2. Consul - 2  
3. Consul - 3  
4. TestDb - Master  
5. TestDb - Slave - 1  
6. TestDb - Slave - 2  
7. Application Layer  
8. Database Load Balancing Layer  
9. Backup Server  
10. ReportingDb - Master  
11. ReportingDb - Slave  
12. Zookeeper - Kafka - 1  
13. Zookeeper - Kafka - 2  
14. MongoDB - Primary  
15. MongoDB - Slave  
16. DelayedDb  
17. PgWatch - PgBadger  

## Project Architecture

![Project Architecture](https://github.com/ProxySeer/PostgresLab/blob/main/Project-Architecture/Architecture.gif)

## Starting Up the Servers

[![Watch the video](https://i.hizliresim.com/2o2po04.PNG)](https://www.youtube.com/watch?v=A_PDvBk6i7Y)

[Click to reach me on LinkedIn](https://github.com/ProxySeer/PostgresLab/blob/main/How%20to%20add%20a%20new%20node/ReadMe.md)
