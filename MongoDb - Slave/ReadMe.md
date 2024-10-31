**Download Link**  <br />

https://drive.google.com/drive/folders/1Puf4vRcxaCGjNi02TzuEMu8NEH2H_Eqm?usp=drive_link

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
