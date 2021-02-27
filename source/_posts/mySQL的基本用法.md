---
title: mySQL基础知识
---

## 什么是数据库

数据库是专门用来管理，存储和组织数据的仓库

## 传统数据的组织结构

传统数据库的组织结构分为：数据薄，数据表，数据行，字段

## 什么是SQL

SQL全称Structured Query Language，即结构化的查询语言，专门用来访问和处理数据库的编程语言

## 查询语句(以下数据表名均为users)
```js
//查询某个数据表的全部内容
select * from users

//查询某个数据表的部分内容
select username,password from users
```

## 插入语句

```js
//插入数据到某个数据表中
insert into users(username,password) values('tom','admin123')
```

## 更新语句

```js
//更新数据表中某条数据
update users set password='888888' where id=2
```

## 删除语句

```js
//删除数据表中某条数据
delete from users where id=3
```

## and和or运算符

```js
//使用多个条件对数据表中的数据进行相关操作,and为多种条件必须同时满足
select * from users where username='jojo' and status=1

//or也是多个条件，但是只需要满足一个即可
select * from users where id=5 or status=1
```

## order by asc(升序) 和 desc(降序)

```js
//通过status属性升序排列数据表
select * from users order by status asc

//通过id属性降序排列数据表
select * from users order by id desc

//升序和降序组合排列(通过status升序后再通过id降序)
select * from users order by status asc,id desc

//where和排序混合使用：id>2且降序排序
select * from users where id>2 order by id desc
```