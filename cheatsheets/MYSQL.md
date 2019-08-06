Create Database:

```
mysql> CREATE DATABASE my_db;
```

Create User:

```
mysql> CREATE USER 'user1'@'%' IDENTIFIED BY 'securepass';
```

Grant User all Permissions to Database:

```
mysql> GRANT ALL PRIVILEGES ON my_db.* TO 'user1'@'%';
```

Flush:

```
mysql> FLUSH PRIVILEGES;
```
