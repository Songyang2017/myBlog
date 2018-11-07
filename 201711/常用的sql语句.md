常用的SQL语句
---
* 创建表  
···sql
create table if not exists 表名(字段1 类型 primary key autoincrement, 字段2 类型, 字段3 类型, 字段4 类型)
···
例：
...sql
create table if not exists gebis(gebi_id int primary KEY AUTO_INCREMENT, gebi_name text, gebi_sex text)
...
