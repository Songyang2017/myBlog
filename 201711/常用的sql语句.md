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
1.删除一条数据  
	
	drop from 表名 where 主键 = 值  
例：  

	drop from students where students_id = 3  
2.删除全部

	drop from 表名  
例：

	drop from students  
#### 查询  
1.查询表中所有的数据  

	select * from 表名  
例：

	select * from students  
2.查询所有数据，但只显示对应的列  

	select 列1, 列2 from 表名  
例：

	select students_name, students_age from students  
3.根据一个条件查询数据  

	select * from 表名 where 字段 = 值  
例：  

	select * from students where students_name = '小张'  
4.根据两个条件查询数据  

	select * from 表名 where 字段1 = 值1 and 字段2 = 值2  
例：

	select * from students where students_sex = '女' and students_age = '13'  
5.根据一个范围查询数据`between and`  

	select * from 表名 where 字段1 > 值1 and 值2  
	select * from 表名 where 字段1 between 值1 and 值2  
例：  
	
	select * from students where students_age > '20'  
	select * from students where students_age between '20' and '30'  
6.查询不在某一个范围内的数据  

	select * from 表名 where students_age not between 值1 and 值2  
例：  
	
	select * from students where students_age not between 20 and 30  
7.根据两个条件中的任何一个查询数据`or`  

	select * from 表名 where 字段1 = 值1 or 字段2 = 值2  
例： 
	
	select * from students where students_age = '12' or students_sex = '女'  
8.根据and和or结合使用查询数据  

	select * from 表名 where 字段1 = 值1 and (字段2 = 值2 or 字段3 = 值3)  
例：  

	select * from students where students_age > '12' and (students_sex = '女' or students_name = '小张')  
9.模糊查询  
在意值的开头，无关后面的内容  

	select * from 表名 where 字段 like 值%  
例：  

	select * from students where students_name like '刘%'  
在意值的结尾，无关前面的内容  

	select * from 表名 where 字段 like %值  
例：

	select * from students where students_name like '%风'    
值的中间，不关系两边的内容  

	select * from 表名 where 字段 like %值%  
例：  
	
	select * from students where student_sex like '%a%'  
否定某个条件查询  

	select * from 表名 where 字段 not like 值%  
例：  

	select * from students where student_sex not like '%a%'  
10.独一无二查询：查询出来的数据都不同  

	select distinct 字段 from 表名  
例：  

	select distinct students_name from students  
11.查询所有数据，但是限制只获取前两条  

	select * from students limit 2  
例：  

	select * from students limit 2  
12.查询所有数据，并对查询结果进行排序（order by）  
某一个字段升序排序`asc`  

	select * from 表名 order by 字段 asc
例：  
	
	select * from students order by student_age asc  
某一个字段升序降序`desc`  

	select * from 表名 order by 字段 desc  
例：  

	select * from students order by student_age desc  
按某一个字段降序排序, 当数据中有相同时，再按另一字段升序  
	
	select * from 表名 order by 字段1 desc, 字段2 asc  
例：  
	
	select * from students order by student_age desc, student_id asc  
