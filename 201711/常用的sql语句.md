常用的SQL语句
---

#### 创建表  
	create table if not exists 表名(字段1 类型 primary key autoincrement, 字段2 类型, 字段3 类型, 字段4 类型)  
例：  

	create table if not exists gebis(gebi_id int primary KEY AUTO_INCREMENT, gebi_name text, gebi_sex text)
#### 删除表
	drop table 表名  
例：  

	drop table wx
#### 插入数据
	insert into 表名(字段1, 字段2, 字段3) values(值1, 值2, 值3)  
例：

	insert into students(students_name, students_sex, students_age) values ('小明', '男', '12')  
#### 更新数据
	update 表名 set 字段1 = 值1, 字段2 = 值2, 字段3 = 值3, where 主键 = 值  
例：

	update students set students_age = '11' where students_id = 6  
#### 删除  
删除一条数据  
	
	drop from 表名 where 主键 = 值  
例：  

	drop from students where students_id = 3  
删除全部

	drop from 表名  
例：

	drop from students  
#### 查询  
查询表中所有的数据  

	select * from 表名  
例：

	select * from students  
查询所有数据，但只显示对应的列：  

	select 列1, 列2 from 表名  
例：

	select students_name, students_age from students
