**Download Link**  <br />

https://drive.google.com/drive/folders/1mx9fSPjBPtfw17VRQZmGeQkfick19H1x?usp=drive_link

**After the virtual machine starts, please follow the steps below.**

**Switch to the postgres user and run pgbackrest command**
```ruby
sudo su - postgres
pgbackrest --stanza=msrsprod_stanza --type=full backup
```

