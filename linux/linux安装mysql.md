> linux安装mysql 以debian为例

查看是否安装MySql
```shell
rpm -qa | grep mysql
```
查看是否安装mariadb
```shell
# 如果是 CentOS7 可以检测出已经安装了 mariadb
rpm -qa | grep mariadb
```
<img src="../img/c821950380254e72a8d2de4b9226b3b8.png" alt="">

移除相关软件
```shell
rpm -e --nodeps mariadb-libs-5.5.68-1.el7.x86_64
```

一、安装Mysql

[下载mysql](https://dev.mysql.com/downloads/mysql/)

解压后安装依赖包

```shell
apt-get install libaio1
```

安装mysql包
```shell
dpkg-preconfigure mysql-community-server_*.deb
```

按步骤设定root密码，加密组件选择5.x

执行命令
```shell
sudo dpkg -i mysql-{common,community-client-plugins,community-client-core,community-client,client,community-server-core,community-server,server}_*.deb
```

有报错使用 `apt-get -f install` 修复

使用`systemctl status mysql`查看mysql服务状态
至此安装MySQL成功