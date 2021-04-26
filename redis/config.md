## Redis 常见配置

### 最大连接数

查看连接数

```
方法1：在redis-cli命令行使用：info clients可以查看当前的redis连接数

127.0.0.1:6379> info clients
#Clients
connected_clients:621
client_longest_output_list:0
client_biggest_input_buf:0
blocked_clients:0
127.0.0.1:6379>

方法2：config get maxclients 可以查询redis允许的最大连接数

127.0.0.1:6379> CONFIG GET maxclients
    ##1) "maxclients"
    ##2) "10000"
127.0.0.1:6379>

```

修改连接数

```
1. 在2.6之后版本，可以修改最大连接数配置，默认10000，可以在redis.conf配置文件中修改
...
# maxclients 10000
...

2.config set maxclients num 可以设置redis允许的最大连接数

127.0.0.1:6379> CONFIG set maxclients 10
OK
127.0.0.1:6379>


3.启动redis.service服务时加参数--maxclients 100000来设置最大连接数限制

redis-server --maxclients 100000 -f /etc/redis.conf
```
