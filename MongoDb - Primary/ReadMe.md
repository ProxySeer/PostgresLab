**Download Link**  <br />

https://drive.google.com/drive/folders/1gQQhBNlnaT6IVUI1nq1dHT7eJyrR2mnZ?usp=drive_link

**After the virtual machine starts, please follow the steps below.** <br />



**Connect to MongoDB.** <br />
```ruby
sudo -i
mongosh
```

**After connecting to MongoDB, run the following commands in the Mongo shell.**
```ruby
rs.status()
use testdb
show collections
db.numbers.find()
```
