# Server Setup Instructions

1. **Copy the Server**  
   Physically copy the `TESTDB1 SANAL` server to another location. After starting it, click on **I copied it**.

2. **Connect to the Server**  
   Once the server is up, connect using the DHCP IP with `ifconfig`.

3. **Update Netplan Configuration**  
   Change the IP in the `addresses:` section of the `/etc/netplan/00-installer-config.yaml` file using `vi`.

4. **Set the Hostname**  
   Set the hostname with:
   ```bash
   hostnamectl set-hostname hostname

5. **Modify Consul Configuration**
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

Save the file.

6. **Update Patroni Configuration**
Edit the patroni.yml file:
```bash
vi /etc/patroni/patroni.yml


Change the following parameters:
```bash
url: https://hostname:8501
postgresql:
  connect_address: "host-ip:5432"
restapi:
  connect_address: host-ip:8009


Save the changes.


Restart Services
Restart both the Consul and Patroni services:


systemctl restart consul
systemctl restart patroni


Update pg_hba Configuration
From the testdb master server, add the new server to the pg_hba section using patronictl:

patronictl edit-config


Add the following lines:

host  replication     standby         host-ip/32     scram-sha-256
host  all             postgres        host-ip/32     scram-sha-256


Save the changes.

Switchover All Servers
Finally, perform a switchover for all servers using:

patronictl switchover






