## Introduce
Redis 就是一个使用 C 语言开发的数据库，不过与传统数据库不同的是 Redis 的数据是存在内存中的 ，也就是它是内存数据库，所以读写速度非常快，因此 Redis 被广泛应用于缓存方向。

如果你要学习 Redis 的话，强烈推荐 《Redis 设计与实现》 和 《Redis 实战》 这两本书。另外，《Redis开发与运维》 这本书也非常不错，既有基础介绍，又有一线开发运维经验分享。


下面是我总结的一些关于并发的小问题，你可以拿来自测：

Redis 和 Memcached 的区别和共同点
为什么要用 Redis/为什么要用缓存？
Redis 常见数据结构以及使用场景分析
Redis 没有使用多线程？为什么不使用多线程？Redis6.0 之后为何引入了多线程？
Redis 给缓存数据设置过期时间有啥用？
Redis 是如何判断数据是否过期的呢？
过期的数据的删除策略了解么？
Redis 内存淘汰机制了解么？
Redis 持久化机制(怎么保证 Redis 挂掉之后再重启数据可以进行恢复)
Redis 缓存穿透、缓存雪崩？
如何保证缓存和数据库数据的一致性？
......

## 基础知识
+ [常见配置](https://github.com/kougazhang/middleware/blob/master/redis/config.md)
