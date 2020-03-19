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
### DDL
* 数据库
  * terminal： mysql -uroot -p
  * 查看所有数据库： SHOW DATABASES
  * 切换（选择要操作的）数据库：USE 数据库名
  * 创建数据库：CREATE DATABASE mydb1
  * 删除数据库：DROP DATABASE mydb1
  * 修改数据库编码：ALTER DATABASE mydb1 CHARACTER SET utf8
