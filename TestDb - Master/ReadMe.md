**Download Link**  <br />

https://drive.google.com/drive/folders/1N1AYYh2g6hpRAmQ3_oH_10OzrMQzRiHG?usp=drive_link

**After the virtual machine starts, please follow the steps below.**

**change user to Root**
```ruby
sudo -i
```
**Start Consul service**

```ruby
systemctl start consul
```

**Start Patroni service**

```ruby
systemctl start patroni
```
**Start Both services Status**
```ruby
systemctl status consul
systemctl status patroni
```

