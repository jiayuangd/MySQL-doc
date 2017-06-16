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

 Field | Type     | Null | Key | Default | Extra |
-------|----------|------|-----|-------- |-------
 sno   | char(9)  | NO   | PRI | NULL    |       |
 sname | char(20) | NO   | UNI | NULL    |       |
sdept  | char(20) | YES  |     | NULL    |       |
 sex   | char(2)  | YES  |     | NULL    |       |
**院校表：**
| Field  | Type        | Null | Key | Default | Extra |
---------|-------------|------|-----|---------+-------+
| cno    | char(4)     | NO   | PRI | NULL    |       |
| cname  | char(40)    | NO   |     | NULL    |       |
| credit | smallint(6) | YES  |     | NULL    |       |


