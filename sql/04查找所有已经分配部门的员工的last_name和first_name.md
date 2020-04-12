# 查找所有已经分配部门的员工的last_name和first_name以及dept_no

[TOC]
## [🎉题解仓库](https://github.com/HANXU2018/nowcoderSQL)
## [🚀题目地址](https://www.nowcoder.com/practice/6d35b1cd593545ab985a68cd86f28671?tpId=82&tqId=29756&tPage=1&rp=&ru=%2Fta%2Fsql&qru=%2Fta%2Fsql%2Fquestion-ranking)

### 🎈题目描述

查找所有已经分配部门的员工的last_name和first_name以及dept_no
CREATE TABLE `dept_emp` (
`emp_no` int(11) NOT NULL,
`dept_no` char(4) NOT NULL,
`from_date` date NOT NULL,
`to_date` date NOT NULL,
PRIMARY KEY (`emp_no`,`dept_no`));
CREATE TABLE `employees` (
`emp_no` int(11) NOT NULL,
`birth_date` date NOT NULL,
`first_name` varchar(14) NOT NULL,
`last_name` varchar(16) NOT NULL,
`gender` char(1) NOT NULL,
`hire_date` date NOT NULL,
PRIMARY KEY (`emp_no`));

| last_name | first_name | dept_no |
| :-------- | :--------- | :------ |
| Facello   | Georgi     | d001    |
| 省略      | 省略       | 省略    |
| Piveteau  | Duangkaew  | d006    |

# 🎉答案

- (SQL 3.7.9)
- 符合MySQL5.7语法规范
- 知识点
  - 连接

```
SELECT 
    employees.last_name,
    employees.first_name,
    dept_emp.dept_no
FROM employees
inner join dept_emp
on dept_emp.emp_no = employees.emp_no
;
```

# 🕵️‍♀️分析

1. 使用select进行展示

2. 查找所有已经分配部门的员工的last_name和first_name以及dept_no

   SELECT 
       employees.last_name,
       employees.first_name,
       dept_emp.dept_no

3. 连接 dept_emp

   FROM employees
   inner join dept_emp

4. 连接条件 on dept_emp.emp_no = employees.emp_no

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