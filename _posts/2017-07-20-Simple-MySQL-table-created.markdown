**目标**
***

1.MySQL 服务处于运行状态;

2.新建数据库的名称为 gradesystem;

3.gradesystem 包含三个表：student、course、mark:
student 表包含3列：sid(主键)、sname、gender；
course 表包含2列：cid(主键)、cname；
mark 表包含4列：mid(主键)、sid、cid、score ，注意与其他两个表主键之间的关系。

4.将数据分别插入到各个表中.

**方案**
***

1.打开服务
```
sudo service mysql start
mysql -u root
```

2.进入mysql建立数据库
```
CREATE DATABASE gradesystem;
```

3.使用数据库并按要求建表
```
use gradesystem;
CREATE TABLE student
(
sid int not null auto_increment,
sname varchar(10) not null,
gender enum('male','female'),
primary key(sid)
);
```
```
CREATE TABLE course
(
cid int not null auto_increment,
cname varchar(10) not null,
primary key(cid)
);
```
```
CREATE TABLE mark
(
mid int not null auto_increment,
sid int,
cid int,
score int not null,
primary key(mid),
constraint foreign key(sid) references student(sid),
constraint foreign key(cid) references course(cid)
);
```

4.键入数据
