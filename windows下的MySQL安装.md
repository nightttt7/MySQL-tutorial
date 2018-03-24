# windows下的MySQL安装
1. 下载MySQL:  
[下载地址](https://dev.mysql.com/downloads/mysql/) -> Generally Available (GA) Releases -> Microsoft Windows -> 32-bit/64-bit(选择对应的32位/64位 windows) -> ZIP Archive -> Download  
![如何下载](https://raw.githubusercontent.com/nightttt7/MySQL-tutorial/master/imgs/1.png)

2. 解压MySQL:  
解压到指定文件夹,并将其中的/bin路径添加至环境变量:  
右键计算机 -> 高级系统设置 -> 环境变量 -> 系统变量 -> Path -> 在末尾添加完整的/bin路径(谨慎操作,不要删改已有值)  
![如何添加环境变量](https://raw.githubusercontent.com/nightttt7/MySQL-tutorial/master/imgs/2.png)

3. 安装MySQL:
    1. 打开命令提示符
    2. 路径变为完整的/bin路径  
    ![如何变更路径](https://raw.githubusercontent.com/nightttt7/MySQL-tutorial/master/imgs/3.png)
    3. 输入以下语句
    ```
    mysqld install 
    mysqld --initialize --user=mysql --console # 会给出初始密码
    net start mysql #启动服务
    ```

4. 初始化MySQL
    1. 命令提示符中输入以下语句  
    ```
    mysql -uroot -p初始密码 #登录,使用刚才给出的初始密码
    set password=password('新密码'); #修改密码
    show variables like '%char%'; #查看默认编码
    set global character_set_database='utf8'; # 如果只是临时更改默认编码为utf-8
    exit #退出mysql 
    ```
    2. 更改默认编码,在mysql目录下添加my.ini文件,文件内容如下:
    ```
    [mysqld]
    character-set-server = utf8
    [client]
    default-character-set = utf8
    ```
    3. 命令提示符中输入以下语句
    ```
    net stop mysql #关闭服务
    net start mysql #启动服务
    ```

5. ==可以开始使用MySQL了==