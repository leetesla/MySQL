# MySQL
MySQL优化

### Optimization Overview  优化概览
### 1.Optimizing SQL Statements  优化SQL语句(https://github.com/o1egl/paseto)
- 1.1 Optimizing SELECT Statements  优化SELECT语句
    + (1)WHERE Clause Optimization  WHERE子句优化
    + (2)Range Optimization  范围查询的优化
    + (3)Index Merge Optimization  索引合并优化
    + (4)Engine Condition Pushdown Optimization  引擎层面的Pushdown优化
    + (5)Index Condition Pushdown Optimization  索引层面的Pushdown优化
    + (6)Nested-Loop Join Algorithms  嵌套循环连接算法
    + (7)Nested Join Optimization  嵌套连接优化
    + (8)Left Join and Right Join Optimization  左连接和右连接优化
    + (9)Outer Join Simplification  简化外连接
    + (10)Multi-Range Read Optimization  多范围查询的优化
    + (11)Block Nested-Loop and Batched Key Access Joins  BNL连接算法和BKA连接算法
    + (12)IS NULL Optimization  IS NULL优化
    + (13)ORDER BY Optimization  ORDER BY优化
    + (14)GROUP BY Optimization  GROUP BY优化
    + (15)DISTINCT Optimization  DISTINCT优化
    + (16)LIMIT Query Optimization  LIMIT查询优化
    + (17)Function Call Optimization  函数调用优化
    + (18)Row Constructor Expression Optimization  行构造器表达式优化
    + (19)Avoiding Full Table Scans  避免全表扫描
- 1.2 Optimizing Subqueries, Derived Tables, and Views  优化子查询，派生表和视图
    + (1)Optimizing Subqueries with Semi-Join Transformations  使用半连接代替子查询
    + (2)Optimizing Subqueries with Materialization  使用Materialization优化子查询
    + (3)Optimizing Derived Tables  优化派生表
    + (4)Optimizing Subqueries with the EXISTS Strategy  使用EXISTS策略优化子查询
- 1.3 Optimizing INFORMATION_SCHEMA Queries  优化INFORMATION_SCHEMA查询
- 1.4 Optimizing Data Change Statements  优化INSERT/UPDATE/DELETE语句
    + (1)优化INSERT语句
    + (2)优化UPDATE语句
    + (3)优化DELETE语句
- 1.5 Optimizing Database Privileges  优化数据库权限
    + 权限设置越复杂，SQL语句的开销就越大。简化由GRANT语句建立的权限，可以使MySQL在客户端执行语句时减少权限检查的开销。
- 1.6 Other Optimization Tips  其他的优化建议

### 2.Optimization and Indexes  优化索引
- 2.1 How MySQL Uses Indexes  MySQL是如何使用索引的
- 2.2 Primary Key Optimization  主键索引优化
- 2.3 Foreign Key Optimization  外键优化
- 2.4 Column Indexes  列索引
- 2.5 Multiple-Column Indexes  复合索引
- 2.6 Verifying Index Usage  查看索引使用情况
- 2.7 InnoDB and MyISAM Index Statistics Collection  InnoDB和MyISAM表索引的统计信息
- 2.8 Comparison of B-Tree and Hash Indexes  B-Tree和Hash索引的比较
- 2.9 Use of Index Extensions  索引扩展的使用


### 3.Optimizing Database Structure  优化数据库结构
- 3.1 Optimizing Data Size  优化数据大小
- 3.2 Optimizing MySQL Data Types  优化数据类型
    + (1)Optimizing for Numeric Data  数值类型的优化
    + (2)Optimizing for Character and String Types  字符串类型的优化
    + (3)Optimizing for BLOB Types  BLOB类型的优化
    + (4)Using PROCEDURE ANALYSE  使用PROCEDURE ANALYSE来选择最佳数据类型
- 3.3 Optimizing for Many Tables  多张表的优化
    + (1)How MySQL Opens and Closes Tables  MySQL是如何打开和关闭表的
    + (2)Disadvantages of Creating Many Tables in the Same Database 在同一数据库中创建大量表的缺点
- 3.4 Internal Temporary Table Use in MySQL  临时表的使用


### 4.Optimizing for InnoDB Tables  InnoDB表的优化
- 4.1 Optimizing Storage Layout for InnoDB Tables  优化InnoDB表的存储方式
- 4.2 Optimizing InnoDB Transaction Management  优化InnoDB事务管理
- 4.3 Optimizing InnoDB Read-Only Transactions  优化InnoDB只读事务
- 4.4 Optimizing InnoDB Redo Logging  优化InnoDB还原日志
- 4.5 Bulk Data Loading for InnoDB Tables  InnoDB表加载大量数据的优化
- 4.6 Optimizing InnoDB Queries  InnoDB查询的优化
- 4.7 Optimizing InnoDB DDL Operations  InnoDB DDL操作的优化
- 4.8 Optimizing InnoDB Disk I/O  InnoDB磁盘I/O的优化
- 4.9 Optimizing InnoDB Configuration Variables  InnoDB配置变量的优化
- 4.10 Optimizing InnoDB for Systems with Many Tables  系统有多个表时InnoDB的优化


### 5.Optimizing for MyISAM Tables  MyISAM表的优化
- 5.1 Optimizing MyISAM Queries  优化MyISAM表的查询
- 5.2 Bulk Data Loading for MyISAM Tables  MyISAM表加载大量数据的优化
- 5.3 Optimizing REPAIR TABLE Statements  优化REPAIR TABLE语句


### 6.Optimizing for MEMORY Tables  MEMORY表的优化


### 7.Understanding the Query Execution Plan  分析查询执行计划
- 7.1 Optimizing Queries with EXPLAIN  用EXPLAIN分析查询语句
- 7.2 EXPLAIN Output Format  EXPLAIN语句输出格式
- 7.3 Extended EXPLAIN Output Format  扩展EXPLAIN语句输出格式
- 7.4 Estimating Query Performance  评估查询性能


### 8.Controlling the Query Optimizer 管理查询优化器
- 8.1 Controlling Query Plan Evaluation  控制查询计划的评估配置
- 8.2 Switchable Optimizations  可切换的优化策略
- 8.3 Index Hints  索引提示


### 9.Buffering and Caching  缓冲和缓存
- 9.1 InnoDB Buffer Pool Optimization  InnoDB缓冲池优化
- 9.2 The MyISAM Key Cache  MyISAM索引缓存
    + (1)Shared Key Cache Access  索引缓存的共享访问
    + (2)Multiple Key Caches  多个索引缓存
    + (3)Midpoint Insertion Strategy  中点插入策略
    + (4)Index Preloading  索引预加载
    + (5)Key Cache Block Size  索引缓存的区块大小
    + (6)Restructuring a Key Cache  重建索引缓存
- 9.3 The MySQL Query Cache  MySQL查询缓存
    + (1)How the Query Cache Operates  查询缓存是如何发挥作用的
    + (2)Query Cache SELECT Options  SELECT语句中有关查询缓存的两个选项
    + (3)Query Cache Configuration  查询缓存配置
    + (4)Query Cache Status and Maintenance  查询缓存状态和维护
- 9.4 Caching of Prepared Statements and Stored Programs 已处理语句和存储程序的缓存


### 10.Optimizing Locking Operations  优化锁操作
- 10.1 Internal Locking Methods  内部锁操作
- 10.2 Table Locking Issues  表的锁定问题
- 10.3 Concurrent Inserts  批量插入
- 10.4 Metadata Locking  元数据锁
- 10.5 External Locking  外部锁


### 11.Optimizing the MySQL Server  优化MySQL服务器
- 11.1 System Factors  系统因素
- 11.2 Optimizing Disk I/O  优化磁盘I/O
- 11.3 Using Symbolic Links  使用符号链接
    + (1)Using Symbolic Links for Databases on Unix  在Unix上的数据库中使用符号链接
    + (2)Using Symbolic Links for MyISAM Tables on Unix  在Unix上的MyISAM表中使用符号链接
    + (3)Using Symbolic Links for Databases on Windows  在Windows上的数据库中使用符号链接
- 11.4 Optimizing Memory Use  优化内存使用
    + (1)How MySQL Uses Memory  MySQL是如何使用内存的
    + (2)Enabling Large Page Support  启用大页面支持
- 11.5 Optimizing Network Use  优化网络使用
    + (1)How MySQL Uses Threads for Client Connections  MySQL客户端连接是如何使用线程的
    + (2)DNS Lookup Optimization and the Host Cache  DNS查询优化和主机缓存


### 12.Measuring Performance(Benchmarking)  性能测试(Benchmarking)
- 12.1 Measuring the Speed of Expressions and Functions  测试表达式和函数的速度
- 12.2 The MySQL Benchmark Suite  MySQL基准测试套件
- 12.3 Using Your Own Benchmarks  使用你自己的基准测试
- 12.4 Measuring Performance with performance_schema  使用performance_schema测试性能


### 13.Examining Thread Information  查看线程信息
- 13.1 Thread Command Values  线程的指令值
- 13.2 General Thread States  通用线程状态
- 13.3 Delayed-Insert Thread States  延迟插入的线程状态
- 13.4 Query Cache Thread States  查询缓存的线程状态
- 13.5 Replication Master Thread States  复制中主库的线程状态
- 13.6 Replication Slave I/O Thread States  复制中从库I/O的线程状态
- 13.7 Replication Slave SQL Thread States  复制中从库SQL的线程状态
- 13.8 Replication Slave Connection Thread States  复制中从库连接的线程状态
- 13.9 NDB Cluster Thread States  NDB集群的线程状态
- 13.10 Event Scheduler Thread States  事件调度器的线程状态



