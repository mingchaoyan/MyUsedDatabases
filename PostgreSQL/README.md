# PostgreSQL

## 历史
* 发行 1995年5月1日
* 作者 PostgreSQL Global Development Group

## 特性

## 数据库管理

### 安装配置
* 配置远程访问
```shell
pg_hba.conf：配置对数据库的访问权限，
postgresql.conf：配置PostgreSQL数据库服务器的相应的参数。
```

### 简单命令

#### 基本
* 初始化cluster
```shell
$ /usr/local/pgsql/bin/initdb -D /usr/local/pgsql/data
```
* 启动数据库服务器
```shell
$ /usr/local/pgsql/bin/postgres -D /usr/local/pgsql/data >logfile 2>&1 &
```
* 创建数据库
```shell
$/usr/local/pgsql/bin/createdb test
```
* 客户端连接 test 数据库
```shell
$ /usr/local/pgsql/bin/psql test
```
* 退出客户端
```shell
=# ctrl+d or \q
```



#### 数据库用户相关


* 创建数据库用户
```shell
CREATE USER dbuser WITH PASSWORD 'password';
```

* 赋予dbuser数据库所有权限
```shell
GRANT ALL PRIVILEGES ON DATABASE exampledb to dbuser;
```
* 赋予 flux 数据库超级用户权限
```shell
 ALTER ROLE flux WITH Superuser;
```
* 修改用户密码
```shell 
=# alter user postgres with password '123456'
``` 

#### 备份/恢复
* 备份
```shell
pg_dump dbname > outfile
```
* 恢复
```shell
psql dbname < infile
```

## SQL

## 驱动(ORM)
* JavaScript:  [Sequelize](http://docs.sequelizejs.com/en/latest/)