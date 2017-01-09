# Redis

## 历史
* 发行 2009年4月10日
* 作者 Salvatore_Sanfilippo
* ![](https://github.com/mingchaoyan/MyUsedDatabases/blob/master/Redis/Salvatore_Sanfilippo.jpg)

## 特性
* key-value
* 内存数据库

## 数据类型
1. strings
2. hashes
3. lists
4. sets
5. sorted-sets

## 常用命令
1. KEYS key
2. SET key value
3. GET key
4. DEL key
5. TYPE key
6. LPUSH
7. EXISTS key
8. INCR key
9. DECR
10. APPEND key value
11. STRLEN key
12. MGET
13. MSET
14. GETBIT
15. SETBIT
16. BITPOS
17. HSET key field value
18. HGET key field
19. HMSET key field value [field value ...]
20. HMGET key field [field ...]
21. HEXISTS key field 
22. HINCRBY key field increment
23. HDEL key field
24. HKEYS key
25. HVALS key
26. HLEN key
27. LPUSH key value
28. RPUSH key value

## 事务
* multi, exec 命令
* 原理 “将多个命令打包， 然后一次性、按顺序地执行”的机制，
    并且事务在执行的期间不会主动中断 —— 服务器在执行完事务中的所有命令之后，
    才会继续处理其他客户端的其他命令( 队列)
* Redis 的事务保证了 ACID 中的一致性（C）和隔离性（I），但并不保证原子性（失败时不能回滚）和持久性（持久性取决于redis本身）
## 数据库管理

### 安装配置
#### 安装
```
    $ wget http://download.redis.io/releases/redis-3.2.5.tar.gz
    $ tar xzf redis-3.2.5.tar.gz
    $ cd redis-3.2.5
    $ make
    $ make install
```

#### 服务器启动
* 直接启动
```
    redis-server 
```
* 配置启动
```
    redis-server config
```
也可以使用 utils/redis_init_script


### 数据操作
* 清空数据

    - 删除这个db下的数据    

        flushdb 

    - 删除所有

        flushall

## 驱动
* [then-redis](https://github.com/mjackson/then-redis)

## 客户端
* [Redis Commander](http://joeferner.github.io/redis-commander/)
* [medis](http://getmedis.com/)
