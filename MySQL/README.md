# MySQL

## 历史
* 发行 1996
* 作者 MySQL AB

## 特性

## 数据类型

## 事务
* 默认 Repeatable Read

## 数据库管理

### 安装配置

### 简单命令

#### 基本
* 启动数据库服务器
```shell
$ mysqld_safe
```
* 客户端连接 test 数据库
```shell
$ mysql -u root
```
* 创建数据库
```shell
mysql>create database test;
```
* 查看数据库/使用数据库/查看数据表
```shell
mysql>show databses;
mysql>use test;
mysql>show tables;
```
* 设置事务级别
```
mysql>set transaction isolation level read committed;
```
*
#### 数据库用户相关

## SQL

## 驱动(ORM)
