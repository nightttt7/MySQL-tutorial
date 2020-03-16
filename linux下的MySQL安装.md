# linux下的MySQL安装

*以CentOS7为例*

1. [下载MYSQL源安装包](https://dev.mysql.com/downloads/repo/yum/),在这个页面里获取下载地址  
`wget 下载地址`

2. 安装源  
`yum localinstall 安装包`

3. 安装SQL  
`yum install mysql-community-server`

4. 如需安装其他SQL组件  
`yum --disablerepo=\* --enablerepo='mysql*-community*' list available`
`yum install package-name`

5. 第一次启用：
```
# 启用
systemctl start mysqld
# 查看状态
systemctl status mysqld
# 设置开机启动
systemctl enable mysqld
systemctl daemon-reload
# 获取默认密码
grep 'temporary password' /var/log/mysqld.log
# 登陆
mysql -urood -p初始密码 #登录,使用刚才给出的初始密码
# 修改root密码(已经进入mysql的界面)
set password for 'root'@'localhost'='password';('新密码包含大小写数字')
```

6. 配置默认编码为utf8,修改/etc/my.cnf配置文件，在[mysqld]下添加编码配置，如下所示：
- attention! 完成编码配置后再创建数据库

```
[client]
default-character-set = utf8mb4
[mysql]
default-character-set = utf8mb4
[mysqld]
character-set-client-handshake = FALSE
character-set-server = utf8mb4
collation-server = utf8mb4_unicode_ci
```

7. 文件路径
    - 配置文件：/etc/my.cnf  
    - 日志文件：/var/log/mysqld.log 
    - 服务启动脚本：/usr/lib/systemd/system/mysqld.service  
    - datadir=/var/lib/mysql-用户名
    - socket=/var/lib/mysql-用户名/mysql.sock

8. 其他命令
```
# 启用
systemctl start mysqld
# 查看状态
systemctl status mysqld
#重启
systemctl restart mysqld
#　结束
systemctl stop mysqld
#　或者
service mysqld {start|stop|restart|status} 
```