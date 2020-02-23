# 解决WordPress权限不足的问题

## 遇到的问题

“WordPress needs to access your web server. Please enter your ftp credentials to proceed”.然后下面就是让你输入什么FTP账号密码什么的.

## 解决的思路

### WordPress没有写的权限

大部分原因都是这样,因为wordpress的拥有者和所属组不是同一个或者都没有赋予相应的权限.  
一般都是我们用root账户去服务器后台移动文件,那么文件的owner和group都会办成root.所以wordpress的实际启动用户就会没有权利去操控这些文件.  
对于这样情况,我们首先要确定的是wordpress的启动用户是哪个.如果你使用的是Apache,那么可以去`/etc/httpd/conf/httpd.conf`的查看apache使用的用户和用户组,wordpress是和这个一致的.apache默认的用户和用户组都是apache.所以我们可以对于wordpress的文件夹修改其用户和用户组.命令如下  
`chown -R apache /var/www/html/`  
`chgrp -R apache /var/www/html/`  
apache是你查到的apache的启动用户,后面的是你的web服务器的文件目录.

### WordPress认为你是在一个公众服务器上

可能这个服务器同时被多个人使用,那么也可能会出现这种问题,这时候只要`wp-config.php`中加入以下代码即可.  
`$method = 'direct';`

### 阻止WordPress的检查

这个可能就是一个掩耳盗铃的办法,但是在很多时候也是有效的.  
直接在`wp-config.php`中加入以下内容  
`define('FS_METHOD', 'direct');`

总的来说,大部分原因都是第一种情况,wordpress用户及用户组的权限不足.
