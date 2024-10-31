**Download Link**  <br />

https://drive.google.com/drive/folders/1x4ZS7PzsQzvNPVf7FyeC_NzqoLq0ntcD?usp=drive_link

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
**Check the cluster status with Patroni**
```ruby
patronictl list
```
