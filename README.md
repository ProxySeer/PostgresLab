
  **!!! The architecture below is set up on virtual servers and ready to run. !!!  All virtual machines have their own download links available in the README.md file within their respective folders, and all commands to be executed after starting the virtual machines are also included.** <br />
  
  **Please read the README.md file in each folder after starting the virtual machines.** <br />

  **Entire structure below, designed to be suitable for HA/DR solutions, on virtual machines. While doing these installations, I used a total of 17 virtual machines. The setup includes the following technologies. All server installations were performed on Ubuntu.**
    
    **Multiple HAProxy <br />
      Multiple PgBouncer <br />
      PostgreSQL Cluster <br />
      Consul Cluster <br />
      Patroni <br />
      PgBackRest <br />
      PgWatch <br />
      PgBadger <br />
      Logical Replication <br />
      Debezium - Zookeeper - Kafka Cluster <br />
      MongoDB Cluster <br />**



**The total size is around 400 GB. Each server has the same configuration, requiring a minimum of 17 GB RAM. Additionally, to ensure the structure works correctly, please watch the video(Starting up the servers) I’ve prepared before starting the servers; otherwise, they    may not work. You need to follow the steps in the video in order. This setup will provide you with numerous opportunities for testing and learning --- > [ click to add a new node to the cluster]https://github.com/ProxySeer/PostgresLab/blob/main/How%20to%20add%20a%20new%20node/ReadMe.md).** 
   
   **Order of starting the virtual machines.** <br />
   
   **1- Consul - 1 <br />
   2- Consul - 2 <br />
   3- Consul - 3 <br />
   4- TestDb - Master <br />
   5- TestDb - Slave - 1 <br />
   6- TestDb - Slave - 2 <br />
   7- Application Layer <br />
   8- Database LoadBalacing Layer <br />
   9- Backup Server <br />
   10- ReportingDb - Master <br />
   11- ReportingDb - Slave <br />
   12- Zookeeper - Kafka - 1 <br />
   13- Zookeeper - Kafka - 2 <br />
   14- MongoDB - Primary <br />
   15- MongoDB - Slave <br /> 
   16- DelayedDb <br />
   17- PgWatch - PgBadger <br />**

   
 **Project-Architecture** <br />
 
![](https://github.com/ProxySeer/PostgresLab/blob/main/Project-Architecture/Architecture.gif)

 **Starting up the servers** <br />

[![Watch the video](https://i.hizliresim.com/2o2po04.PNG)](https://www.youtube.com/watch?v=A_PDvBk6i7Y)

  
 [Click to reach me on LinkedIn](https://github.com/ProxySeer/PostgresLab/blob/main/How%20to%20add%20a%20new%20node/ReadMe.md)
