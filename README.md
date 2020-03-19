# database-learning
### 1.1 理解数据库
* RDBMS = Relational database management system = 管理员（manager） + 仓库（database）
* database = N 个table
* table：
  * 表结构： 定义表的列名和列类型！
  * 表记录： 一行一行的记录！

### 1.2 SQL
* 什么是SQL: 结构化查询语言(Structured Query Language)
* SQL语法：
  * SQL语法可以在单行或多行书写，以分号结尾
  * 可以使用空格和缩进来增强语句的可读性
  * MySQL 不区别大小写，建议使用大写
* SQL语句分类：
  * DDL (Data Definition Language): 数据定义语言， 用来定义数据库对象： 库，表，列等；-> 创建，删除，修改：库， 表结构！！！
  * DML (Data Manipulation Language): 数据操作语言， 用来定义数据库记录（数据）-> 增， 删， 改：表记录
  * DCL (Data Control Language): 数据控制语言， 用来定义访问权限和安全级别；
  * DQL (Data Query Language): 数据查询语言， 用来查询记录（数据）
  * 总结：
    *ddl：数据库或表的结构操作 
    *dml：对表的纪录进行更新（增， 删， 改）
    *dql：对表的记录的查询
    *dcl：对用户的创建，及授权！
### 1.3 DDL
* 数据库
  * terminal： mysql -uroot -p
  * 查看所有数据库： SHOW DATABASES;
  * 切换（选择要操作的）数据库：USE 数据库名
  * 创建数据库：CREATE DATABASE mydb1;
  * 删除数据库：DROP DATABASE mydb1;
  * 修改数据库编码：ALTER DATABASE mydb1 CHARACTER SET utf8;
* 常见的数据类型（列类型）
  * int：整数
  * double：浮点型，例如double（5，2）表示最多5位，其中必须有2位小数，即最大值999.99
  * decimal：浮点型，在表单钱方面使用该类型，因为不会出现精度缺失问题
  * char：固定长度字符串类型，char（255）
  * varchar：可变长度字符串类型，varchar（65535），zhangSan
  * text（clob）：字符串类型：> 很小 > 小 > 中 > 大
  * blob：字节类型：> 很小 > 小 > 中 > 大
  * date：日期类型，格式为：yyyy-MM-dd
  * time: 时间类型，格式为：hh:mm:ss
  * timestamp: 时间戳类型：有时间表 又有年月日
* 表
  * 创建表：CREATE TABLE [IF NOT EXISTS] 表名（ 列名 列类型，   列名 列类型，  ...  列名 列类型）；
  * 查看当前数据库中所有表格的名称： SHOW TABLES;
  * 查看指定表的创建语句：SHOW CREATE TABLE 表名（了解）；
  * 查看表结构：DESC 表名；
  * 删除表：DROP TABLE 表名；
  * 修改表：前缀：ALTER TABLE 表名； 
    -> 修改之添加列：ALTER TABLE 表名 ADD ( 列名 列类型，   列名 列类型，  ...);
    -> 修改之修改列类型（如果被修改的列已存在数据，那么新的类型可能会影响到已存在数据）：ALTER TABLE 表名 MODIFY 列名 列类型;
    -> 修改之修改列名：ALTER TABLE 表名 CHANGE 原列名 新列名 列类型；
    -> 修改之删除列：ALTER TABLE 表名 DROP 列名；
    -> 修改表名称：ALTER TABLE 原表名 RENAME TO 新表名；
### 1.3 DDL
* 数据库
  * terminal： mysql -uroot -p
  * 查看所有数据库： SHOW DATABASES;
  * 切换（选择要操作的）数据库：USE 数据库名
  * 创建数据库：CREATE DATABASE mydb1;
  * 删除数据库：DROP DATABASE mydb1;
  * 修改数据库编码：ALTER DATABASE mydb1 CHARACTER SET utf8;
* 常见的数据类型（列类型）
  * int：整数
  * double：浮点型，例如double（5，2）表示最多5位，其中必须有2位小数，即最大值999.99
  * decimal：浮点型，在表单钱方面使用该类型，因为不会出现精度缺失问题
  * char：固定长度字符串类型，char（255）
  * varchar：可变长度字符串类型，varchar（65535），zhangSan
  * text（clob）：字符串类型：> 很小 > 小 > 中 > 大
  * blob：字节类型：> 很小 > 小 > 中 > 大
  * date：日期类型，格式为：yyyy-MM-dd
  * time: 时间类型，格式为：hh:mm:ss
  * timestamp: 时间戳类型：有时间表 又有年月日
* 表
  * 创建表：CREATE TABLE [IF NOT EXISTS] 表名（ 列名 列类型，   列名 列类型，  ...  列名 列类型）；
  * 查看当前数据库中所有表格的名称： SHOW TABLES;
  * 查看指定表的创建语句：SHOW CREATE TABLE 表名（了解）；
  * 查看表结构：DESC 表名；
  * 删除表：DROP TABLE 表名；
  * 修改表：前缀：ALTER TABLE 表名； 
    -> 修改之添加列：ALTER TABLE 表名 ADD ( 列名 列类型，   列名 列类型，  ...);
    -> 修改之修改列类型（如果被修改的列已存在数据，那么新的类型可能会影响到已存在数据）：ALTER TABLE 表名 MODIFY 列名 列类型;
    -> 修改之修改列名：ALTER TABLE 表名 CHANGE 原列名 新列名 列类型；
    -> 修改之删除列：ALTER TABLE 表名 DROP 列名；
    -> 修改表名称：ALTER TABLE 原表名 RENAME TO 新表名；
  

