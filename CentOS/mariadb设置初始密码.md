# yum安装mariadb-server设置初始密码

以CentOS为例,安装mariadb-server之后的操作

## 启动mariadb

`systemctl start mysqld`

## 进入数据库

首次进入数据库,直接输入`mysql`命令即可,后面不用加入任何参数,具体的操作操作看下面  

```shell
mysql #进入数据库
use mysql #进入mysql数据表
update user set password=password("你自己的密码")where user='root'; #设置root密码
flush privileges; #刷新数据库及相关用户权限
exit #推出数据库
```

密码设置完成,然后就可以使用`mysql -uroot -p`再输入你刚才设置的密码就可以登录数据库了.
