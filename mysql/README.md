# Navicat 连接出错

使用 mysql-client 连接 

查看当前用户的 plugin 模式
```sql
select user,plugin from mysql.user;
```

切换到低版本的 mysql_native_password

```sql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'root';
```

最后的root 为修改模式后的新密码，可自行更换
