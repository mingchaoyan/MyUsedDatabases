# InfluxDB

## 1. 历史
* 发行 2013年9月24日
* 作者 Errplane

## 1. 特性
* 时序

## 2. 数据类型

## 3. 常用命令

### 3.1 数据库操作

* show databases 显示数据库
* create database test 新建test数据库
* drop database test 删去test数据库
* use test 使用test数据库

### 3.2 表操作

* show measurements 显示所有表
* insert disk_free,hostname=server01 value=442221834240i 1435362189575692182 新建表并插入
* drop measurement disk_free 删除表
* show tag keys from winLevel 查看tag 
* show field keys from winLevel 查看field

## 4. 事务

## 5. 数据库管理

### 5.1 安装配置

    brew install influxdb

    apt-get install influxdb

### 5.2 启动

    sudo brew services start influxdb

    sudo service influxdb start

## 驱动

## 客户端

