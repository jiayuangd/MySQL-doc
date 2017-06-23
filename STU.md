# MySQL-doc
创建STU学生库，建立三个表：
1. 学生信息表
1. 课程表
1. 成绩表
* 学生信息表：

学号 姓名 性别 年龄 所在系
* 课程表：

课程号 课程名 任课教师 学分
* 成绩表：

学号 课程号 成绩            

**学生信息表：**

```sql
create table info( stuId char(20) primary key, name char(32) unique not null, sex char(16)，age char(16)，dept char(20), state char（4） default('1') );
```
学生信息表设计

中文名称 | 字段名|字段属性 | 备注
---------|-------|--------|-----------
学号    | stuId |char(20)|主码
姓名    |name   |char(32)|取唯一值,非空
年龄    |age    |char(16)|非空
性别    |sex    |char(16)|男或女
专业号  |dept   |char(10)|非空
状态    |state  |char(4) |默认值为'1'

 
**课程表：**

```sql
create table course(cno char(4) primary key, cname char(40) not null,
    -> credit char(6), teacher char(45));
```
课程表设计

中文名称 | 字段名 |字段属性 | 备注
---------|--------|--------|---
课程号   |cno    |char(4)  |主码
课程名称 |cname  |char(40) |非空
任课教师 |teacher|char(45) |非空
学分     |credit |char(6)  |非空
**成绩表**

```sql
 create table score(stuId char(32), 
 cno char(4), grade int(10), 
 primary key(stuId,cno), 
 foreign key (stuId) references info(stuId) 
 on delete cascade
 on update cascade, 
 foreign key (cno) references course(cno))
 on delete cascade
 on update cascade;
```
成绩表设计

中文名称 | 字段名 |字段属性 | 备注
---------|-------|---------|----
学号    |stuId   |char(32) |主码
课程号  |cno     |char(4)  |主码
成绩    |grade   |int(10)  |

## 关系图：
![](img/ER图.jpg)


