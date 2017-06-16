# MySQL-doc
创建STU学生库，建立三个表：
1. 学生信息表
1. 院校系
1. 成绩表
学生信息表：
学号 姓名 性别 年龄 所在系
院校表：
学校 学院 课程号 学号
成绩表：
学号 课程号 成绩            

**学生信息表：**

```sql
create table info( sno char(9) primary key, sname char(20) unique not null, sdept char(20) , sex char(2) );
```

 Field | Type     | Null | Key | Default | Extra |
-------|----------|------|-----|-------- |-------
 sno   | char(9)  | NO   | PRI | NULL    |       |
 sname | char(20) | NO   | UNI | NULL    |       |
sdept  | char(20) | YES  |     | NULL    |       |
 sex   | char(2)  | YES  |     | NULL    |       |
 
**课程表：**

```sql
create table course(cno char(4) primary key, cname char(40) not null,
    -> credit smallint);
```

| Field  | Type        | Null | Key | Default | Extra |
---------|-------------|------|-----|---------|------- 
| cno    | char(4)     | NO   | PRI | NULL    |       |
| cname  | char(40)    | NO   |     | NULL    |       |
| credit | smallint(6) | YES  |     | NULL    |       |

**成绩表**
```sql
 create table score(sno char(9), 
 cno char(4), grade smallint, 
 primary key(sno,cno), 
 foreign key (sno) references info(sno), 
 foreign key (cno) references course(cno));
```

| Field | Type        | Null | Key | Default | Extra |
|-------|-------------|------|-----|---------|--------
| sno   | char(9)     | NO   | PRI | NULL    |       |
| cno   | char(4)     | NO   | PRI | NULL    |       |
| grade | smallint(6) | YES  |     | NULL    |       |


