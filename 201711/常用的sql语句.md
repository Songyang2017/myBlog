常用的SQL语句
---

#### 创建表  
	create table if not exists 表名(字段1 类型 primary key autoincrement, 字段2 类型, 字段3 类型, 字段4 类型)  
例如：  

	create table if not exists gebis(gebi_id int primary KEY AUTO_INCREMENT, gebi_name text, gebi_sex text)
#### 删除表
	drop table 表名  
例如：  

	drop table wx
#### 插入数据
	insert into 表名(字段1, 字段2, 字段3) values(值1, 值2, 值3)
例如：

	insert into students(students_name, students_sex, students_age) values ('小明', '男', '12')