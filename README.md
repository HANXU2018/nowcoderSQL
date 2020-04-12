# 🐂牛客网数据库SQL 实战答案解析

# 🚩目录

[TOC]

# 🍭OJ刷题 地址

- [🚀数据库SQL 实战](https://www.nowcoder.com/ta/sql)
- [🎉题解仓库](https://github.com/HANXU2018/nowcoderSQL)

# 题解🔥目录

1. oj平台为[🐂牛客网在线评测平台](https://www.nowcoder.com/ta/sql)
2. 语法规范：🎯**SQLite3.7.9**
3. 题解参考牛客网->[试题广场->讨论区](https://www.nowcoder.com/questionCenter)
4. 参考Git仓库[数据库SQL实战](https://gitee.com/xuthus5/Database-SQL-Actual-Combat)

| 题号 | 知识点       |                             题目                             | 难度 | MySQL规范 |
| ---- | ------------ | :----------------------------------------------------------: | :--: | :-------: |
| 1    | 过滤         | [查找最晚入职员工的所有信息](/sql/01查找最晚入职员工的所有信息.md) |  💛💛  |     💛     |
| 2    | 过滤         | [查找入职员工时间排名倒数第三的员工所有信息](/sql/02查找入职员工时间排名倒数第三的员工所有信息.md) |  💛💛  |     💛     |
| 3    | 连接         |             查找当前薪水详情以及部门编号dept_no              |      |           |
| 4    | 连接         |      查找所有已经分配部门的员工的last_name和first_name       |      |           |
| 5    | 连接         |  查找所有员工的last_name和first_name以及对应部门编号dept_no  |      |           |
| 6    | 连接         |                查找所有员工入职时候的薪水情况                |      |           |
| 7    | 分组         |   查找薪水涨幅超过15次的员工号emp_no以及其对应的涨幅次数t    |      |           |
| 8    | 过滤         |                找出所有员工当前薪水salary情况                |      |           |
| 9    | 连接         | 获取所有部门当前manager的当前薪水情况，给出dept_no,   emp_no以及salary，当前表示to_date=9999-01-01 |      |           |
| 10   | 过滤         |                获取所有非manager的员工emp_no                 |      |           |
| 11   | 连接         |                  获取所有员工当前的manager                   |      |           |
| 12   | 分组聚合     |           获取所有部门中当前员工薪水最高的相关信息           |      |           |
| 13   | 分组聚合     |               从titles表获取按照title进行分组                |      |           |
| 14   | 分组聚合     |               从titles表获取按照title进行分组                |      |           |
| 15   | 过滤         |                       查找employees表                        |      |           |
| 16   | 分组聚合     |   统计出当前各个title类型对应的员工当前薪水对应的平均工资    |      |           |
| 17   | 过滤         |    获取当前薪水第二多的员工的emp_no以及其对应的薪水salary    |      |           |
| 18   | 连接         | 获取当前薪水第二多的员工的emp_no以及其对应的薪水salary，不准使用order   by |      |           |
| 19   | 连接         |    查找所有员工的last_name和first_name以及对应的dept_name    |      |           |
| 20   | 过滤         | 查找员工编号emp_no为10001其自入职以来的薪水salary涨幅值growth |      |           |
| 21   | 连接         |             查找所有员工自入职以来的薪水涨幅情况             |      |           |
| 22   | 分组聚合     |              统计各个部门对应员工涨幅的次数总和              |      |           |
| 23   | 排名         |         对所有员工的薪水按照salary进行按照1-N的排名          |      |           |
|      | 连接         |             获取所有非manager员工当前的薪水情况              |      |           |
| 25   | 连接         |    获取员工其当前的薪水比其manager当前薪水还高的相关信息     |      |           |
| 26   | 连接和分组   |          汇总各个部门当前员工的title类型的分配数目           |      |           |
| 27   | 连接         |       给出每个员工每年薪水涨幅超过5000的员工编号emp_no       |      |           |
| 28   | 连接         | 查找描述信息中包括robot的电影对应的分类名称以及电影数目，而且还需要该分类对应电影数量>=5部 |      |           |
| 29   | 连接         |         使用join查询方式找出没有分类的电影id以及名称         |      |           |
| 30   | 子查询       | 使用子查询的方式找出属于Action分类的所有电影对应的title,description |      |           |
| 31   | 优化         |         获取 select * from employees 对应的执行计划          |      |           |
| 32   | 字符串处理   | 将employees表的所有员工的last_name和first_name拼接起来作为Name |      |           |
| 33   | 表操作       |               创建一个actor表，包含如下列信息                |      |           |
| 34   | 数据操作     |                         批量插入数据                         |      |           |
| 35   | 数据操作     |               批量插入数据，不使用replace操作                |      |           |
| 36   | 表和数据操作 |                     创建一个actor_name表                     |      |           |
| 37   | 索引         |          对first_name创建唯一索引uniq_idx_firstname          |      |           |
| 38   | 视图         |              针对actor表创建视图actor_name_view              |      |           |
| 39   | 索引         |       针对上面的salaries表emp_no字段创建索引idx_emp_no       |      |           |
| 40   | 表操作       |         在last_update后面新增加一列名字为create_date         |      |           |
| 41   | 触发器       |                   构造一个触发器audit_log                    |      |           |
| 42   | 数据操作     |        删除emp_no重复的记录，只保留最小的id对应的记录        |      |           |
| 43   | 数据操作     |          将所有to_date为9999-01-01的全部更新为NULL           |      |           |
| 44   | 数据操作     |   将id=5以及emp_no=10001的行数据替换成id=5以及emp_no=10005   |      |           |
| 45   | 表操作       |              将titles_test表名修改为titles_2017              |      |           |
| 46   | 外键         | 在audit表上创建外键约束，其emp_no对应employees_test表的主键id |      |           |
| 47   | 连接         |            如何获取emp_v和employees有相同的数据no            |      |           |
| 48   | 数据操作     |            将所有获取奖金的员工当前的薪水增加10%             |      |           |
| 49   | 字符串处理   |       针对库中的所有表生成select count(*)对应的SQL语句       |      |           |
| 50   | 字符串处理   | 将employees表中的所有员工的last_name和first_name通过(')连接起来 |      |           |
| 51   | 字符串处理   |          查找字符串'10,A,B' 中逗号','出现的次数cnt           |      |           |
| 52   | 字符串处理   |                 获取Employees中的first_name                  |      |           |
| 53   | 聚合函数     |                     按照dept_no进行汇总                      |      |           |
| 54   | 聚合函数     |  查找排除当前最大、最小salary之后的员工的平均工资avg_salary  |      |           |
| 55   | 关键字       |       分页查询employees表，每5行一页，返回第2页的数据        |      |           |
| 56   | 连接         |                     获取所有员工的emp_no                     |      |           |
| 57   | 子查询       |    使用含有关键字exists查找未分配具体部门的员工的所有信息    |      |           |
| 58   | 视图         |       获取employees中的行数据，且这些行也存在于emp_v中       |      |           |
| 59   | 条件语句     |                   获取有奖金的员工相关信息                   |      |           |
| 60   | 表的复用     |               统计salary的累计和running_total                |      |           |
| 61   | 表的复用     |          对于employees表中，给出奇数行的first_name           |      |           |

# 🚅急速零基础入门数据库

## **🛴基本概念**

1. **键**          就是数据表中的列或者列的组合。
2. **主键**          表中可以唯一确定本表中某行记录的列或者列的组合。
                     例如或者身份证号码唯一确定一个人；用户ID+发票号码唯一确认某次交易。
3. **外键**          表中的某列或者某些列的组合是其他表的主键。
                     其作用是为了建立和其他表的关联关系。
4. **连接**          将几个个有关联的表（其中一个表的主键是其他表的外键）建立连接关系，形成一个临时表以供它用。
                     建立连接的主键/外键是建立连接的依据。
5. **内连接**    将进行连接的表以建立连接的依据为中心，将这些表取交集，交集就是内连接的结果。
                     作用就是找出在两张表中都有的记录。
6. **外连接**    连接的动作和内连接一样，结果不同。将表进行交集之后，取交集中的记录以及某表中除交集之外的所有记录。包括左连接和右连接。
                     例如A表左连接B表，实际上就是取交集在B表中所有字段的值+A表内容。
7. **自连接**    连接动作同上，只不过是在一张表中进行。
                     这样的情况适用于表中的2个字段互相有关联，并且要对这种关联进行处理时。

## **🚲基本SQL语句**

- **Select From** **Where 从某些表中选取符合某条件的记录**
Select Distinct name,id From table  Where Num=6 选取名为table的表中所有Num字段等于6的记录，并且只显示name、id列的内容。如果要全部显示，可以使用Select *。Distict是表示重复的结果只保留一个。
- **Join** **进行表的各种连接**
  Select name,id FROM table1 [INNER|LEFT OUTER|RIGHT OUTER] JOIN table2 ON table1.id [>|<|>=|<=|=] table2.id 这是进行内连接/左外联/右外联的表示方式，其中id就是建立连接的依据，on后面的部分是选择对象的筛选条件。例如，如果是“=”，表示在两个表中id相同的记录中进行查询
- **Order By** **将查询结果进行排序**格式order by table.name Desc，将结果按照表table中的字段name进行降序排序。默认不标明排序方式的是升序。
- **Group By** **Having**将查询结果按照Group By的条件进行分组，Having 增加结果显示的约束条件，即在上述查询结果中符合某条件的记录才能显示。
  Group By table.name Having tabel.number>2，即将结果中table的name字段相同的记录合为一条记录，并且只有table.number大于2的分组符合显示条件。

## **🛵基本常用函数**

- Sum（）计算某些记录的和
- AVG（）计算某些记录的平均值
- Count（）计算符合某些条件的记录的个数
- Max（）筛选出某些值中的最大值
- Min（）筛选出某些值中的最小值



# 📫联系方式

1. 代码仓库

	- github🍦  [HANXU2018](https://github.com/HANXU2018)

	- gitee🍦 [hanxu051](https://gitee.com/hanxu051)

2. 个人博客

	- [csdn🍦 [韩旭051]](https://hanxu.blog.csdn.net/)
	- [博客园🍦 [韩旭的笔记本]](https://www.cnblogs.com/hx97/)

3. 邮箱

	- QQ邮箱:🍦[1076998404@qq.com](1076998404@qq.com)

