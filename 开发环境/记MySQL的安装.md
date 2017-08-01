记MySQL的安装   
2017/7/27 14:45:41  

# 记MySQL的安装
## 程序版本

    Server version: 5.7.18 MySQL Community Server (GPL)


## 所需文件：   
    mysql-5.7.18-winx64.zip

## 安装过程 

1. 解压文件到`D:\Programs Files\MySQL\`  文件夹下；
2. 设置环境变量：`Path` 中添加路径：`D:\Programs Files\MySQL\mysql-5.7.18-winx64\bin` ;
3. 由于我使用的zip包中没有data文件夹和my-default.ini配置文件，所以在根文件夹下新建data文件夹和my.ini;
4. 在my.ini中保存以下代码：


    >     [mysql]
    >     # 设置mysql客户端默认字符集
    >     default-character-set=utf8 
    >     [mysqld]
    >     #设置3306端口
    >     port = 3306 
    >     # 设置mysql的安装目录
    >     basedir=D:\Program Files\mysql-5.7.18-winx64
    >     # 设置mysql数据库的数据的存放目录
    >     datadir=D:\Program Files\mysql-5.7.18-winx64\data
    >     # 允许最大连接数
    >     max_connections=200
    >     # 服务端使用的字符集默认为8比特编码的latin1字符集
    >     character-set-server=utf8
    >     # 创建新表时将使用的默认存储引擎
    >     default-storage-engine=INNODB


5. 然后打开带管理员模式的cmd（win10中右键win键即可），依次输入：     

    mysqld -install  
    mysqld --initialize  
    net start mysql  
    
结果如图所示。
图片


