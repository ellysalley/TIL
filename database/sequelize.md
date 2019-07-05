## sequelize, mysql2, and mysql8.0

* Sequelize depends on "mysql2" library, which doesn't support mysql 8.0
* Replace 'password' with your new password
```
mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
