**Download Link**  <br />

https://drive.google.com/drive/folders/1t9xWBecw2YQ3DeTImy1DgUQs8Dyhwjhg?usp=drive_link

**After the virtual machine starts, please follow the steps below.**

**Switch to the root user**
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
**Check the status of both services**
```ruby
systemctl status consul
systemctl status patroni
```
