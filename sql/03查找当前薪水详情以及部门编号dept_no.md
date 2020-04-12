# 查找当前薪水详情以及部门编号dept_no

[TOC]
## [🎉题解仓库](https://github.com/HANXU2018/nowcoderSQL)
## [🚀题目地址](https://www.nowcoder.com/practice/c63c5b54d86e4c6d880e4834bfd70c3b?tpId=82&tqId=29755&tPage=1&rp=&ru=%2Fta%2Fsql&qru=%2Fta%2Fsql%2Fquestion-ranking)

### 🎈题目描述

查找各个部门当前(to_date='9999-01-01')领导当前薪水详情以及其对应部门编号dept_no
CREATE TABLE `dept_manager` (
`dept_no` char(4) NOT NULL,
`emp_no` int(11) NOT NULL,
`from_date` date NOT NULL,
`to_date` date NOT NULL,
PRIMARY KEY (`emp_no`,`dept_no`));
CREATE TABLE `salaries` (
`emp_no` int(11) NOT NULL,
`salary` int(11) NOT NULL,
`from_date` date NOT NULL,
`to_date` date NOT NULL,
PRIMARY KEY (`emp_no`,`from_date`));

### 输出描述

| emp_no | salary | from_date  | to_date    | dept_no |
| :----- | :----- | :--------- | :--------- | :------ |
| 10002  | 72527  | 2001-08-02 | 9999-01-01 | d001    |
| 10004  | 74057  | 2001-11-27 | 9999-01-01 | d004    |
| 10005  | 94692  | 2001-09-09 | 9999-01-01 | d003    |
| 10006  | 43311  | 2001-08-02 | 9999-01-01 | d002    |
| 10010  | 94409  | 2001-11-23 | 9999-01-01 | d006    |

# 🎉答案

- (SQL 3.7.9)
- 符合MySQL5.7语法规范
- 知识点
  - 连接

```
SELECT s.emp_no	,s.salary,s.from_date,s.to_date,d.dept_no
FROM salaries s
inner join dept_manager d
on d.emp_no = s.emp_no
and  d.to_date = '9999-01-01'
and s.to_date= '9999-01-01'
;

```

# 🕵️‍♀️分析

1. 过滤使用select

2. 显示内容为s.emp_no	,s.salary,s.from_date,s.to_date,d.dept_no

3. salaries 表和  dept_manage表进行关联  使用 inner join 内关联

   FROM salaries s
   inner join dept_manager d

4. 关联方式为 d.emp_no 和 s.emp_no 相等

    on d.emp_no = s.emp_no

5. 限定当前 当前(to_date='9999-01-01')

   and  d.to_date = '9999-01-01'
   and s.to_date= '9999-01-01'

# 🍭OJ刷题 地址

- [🚀数据库SQL 实战](https://www.nowcoder.com/ta/sql)
- [🎉题解仓库](https://github.com/HANXU2018/nowcoderSQL)


# 📫联系方式

1. 代码仓库

	- github🍦  [HANXU2018](https://github.com/HANXU2018)

	- gitee🍦 [hanxu051](https://gitee.com/hanxu051)

2. 个人博客

	- [csdn🍦 [韩旭051]](https://hanxu.blog.csdn.net/)
	- [博客园🍦 [韩旭的笔记本]](https://www.cnblogs.com/hx97/)

3. 邮箱

	- QQ邮箱:🍦[1076998404@qq.com](1076998404@qq.com)