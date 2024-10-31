**Download Link**  <br />

https://drive.google.com/drive/folders/1Mm94Tg0jwR3GHzvPk3IcAnJ4hIBImF3M?usp=drive_link

**After the virtual machine starts, please follow the steps below.**

**Switch to the root user**
```ruby
sudo -i
```
**Start HaProxy service**

```ruby
systemctl start haproxy
```

**!! To check that all ports are directed to the standby and production databases, visit the address 192.168.217.138 in your web browser. !!**
