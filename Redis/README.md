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

## 事务
* multi, exec 命令
* 原理 “将多个命令打包， 然后一次性、按顺序地执行”的机制，
    并且事务在执行的期间不会主动中断 —— 服务器在执行完事务中的所有命令之后，
    才会继续处理其他客户端的其他命令( 队列)
* Redis 的事务保证了 ACID 中的一致性（C）和隔离性（I），但并不保证原子性（失败时不能回滚）和持久性（持久性取决于redis本身）
## 数据库管理

## 驱动
* [then-redis](https://github.com/mjackson/then-redis)
