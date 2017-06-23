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
create table info( stuId char(9) primary key, sname char(20) unique not null, sdept char(20) , sex char(2) );
```


 
**课程表：**

```sql
create table course(cno char(4) primary key, cname char(40) not null,
    -> credit smallint);
```


**成绩表**

```sql
 create table score(sno char(9), 
 cno char(4), grade smallint, 
 primary key(sno,cno), 
 foreign key (sno) references info(sno) , 
 foreign key (cno) references course(cno));
```




