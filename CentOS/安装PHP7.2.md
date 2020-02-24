# CentOS安装PHP7.2

目前PHP的稳定版本应该是到了7.4,但是7.4版本`yum`并没有提供一键式的安装包.需要自己手动编译安装.对于我们这种Linux新手可不是特别友好,所以,这里以7.2版本为例,简单介绍一下相对傻瓜的安装.值得注意的是,7.2好像是不兼容7.1版本的.因为我有一个特别喜欢的WordPress主题是不支持7.2及以上版本的.

## 获取RPM

`rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm`  
`rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm`

## 安装

`yum -y install php72w`

### 安装相关的拓展

基本的拓展  
`yum -y install php72w-cli php72w-common php72w-devel php72w-mysql`  
wordpress可能需要的拓展  
`yum -y install php72w-gd php72w-imap php72w-ldap php72w-odbc php72w-pear php72w-xml php72w-xmlrpc`  
如果还需要其他的拓展,可以在命令好输入`PHP -m`查看支持的拓展

安装完成
