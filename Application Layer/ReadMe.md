
**Download Link**  <br />

https://drive.google.com/drive/folders/18FYSgwlpqujG_1WbvL2djJmT5odnqVQz?usp=drive_link

**After the virtual machine starts, please follow the steps below.**

**Switch to the root user**
```ruby
sudo -i
```
**Start HaProxy service**

```ruby
systemctl start haproxy
```

**Start Pgbouncer service**

```ruby
systemctl start pgbouncer
```
**Start Pgbouncer1 service**

```ruby
systemctl start pgbouncer1
```
**Start Pgbouncer2 service**

```ruby
systemctl start pgbouncer2
```
**Start Pgbouncer3 service**

```ruby
systemctl start pgbouncer3
```
**!! After all services have been started, check the services by going to the address 192.168.217.137 in your web browser !!**


