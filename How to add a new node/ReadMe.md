# Server Setup Instructions

1. **Copy the Server**  
   Physically copy the `TestDb-Slave-1` server to another location. After starting it, click on **I copied it**.

2. **Connect to the Server**  
   Once the server is up, connect using the DHCP IP with `ifconfig`.

3. **Update Netplan Configuration**  
   Change the IP in the `addresses:` section.
   ```bash
   vi /etc/netplan/00-installer-config.yaml
   ```
5. **Set the Hostname**  
   Set the hostname with:
   ```bash
   hostnamectl set-hostname hostname
   ```
6. **Modify Consul Configuration**

   Edit the consul.json file:
   ```bash
   vi /etc/consul.d/consul.json
   ```

   Update the following:
   ```bash
   {
     "node_name": "hostname",
     "bind_addr": "host-ip",
     "client_addr": "127.0.0.1 host-ip"
   }
   ```

   Save the file.

7. **Update Patroni Configuration**
   Edit the patroni.yml file:
   ```bash
   vi /etc/patroni/patroni.yml
   ```
   Change the following parameters:
   ```bash
   url: https://hostname:8501
   postgresql:
     connect_address: "host-ip:5432"
   restapi:
     connect_address: host-ip:8009
   ```
   Save the changes.


8. **Restart Services**
   Restart both the Consul and Patroni services:
   ```bash
   systemctl restart consul
   systemctl restart patroni
   ```

9. **Update pg_hba Configuration**
   From the testdb master server, add the new server to the pg_hba section using patronictl:
   ```bash
   patronictl edit-config
   ```
   Add the following lines:
   ```bash
   host  replication     standby         host-ip/32     scram-sha-256
   host  all             postgres        host-ip/32     scram-sha-256
   ```
   Save the changes.

10. **Switchover All Servers**
   Finally, perform a switchover for all servers using:
   ```bash
   patronictl switchover
   ```






