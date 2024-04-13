# 校园娱乐共享平台

技术栈：SpringBoot+MyBatis-Plus+MySQL+Redis+RabbitMQ

- 基于 SpringBoot 整合整合 MyBatis-Plus 完成项目基本业务逻辑代码的编写；
- 通过使用 Redis作为会话存储，结合拦截器实现用户的登录校验和权限刷新，解决集群模式下的解决集群模式下的 Session 共享问题；共享问题；
- 通过先更新数据库再删除缓存先更新数据库再删除缓存的策略，保障商铺缓存与数据库之间的数据一致性；
- 使用布隆过滤器解决查询商铺时存在的缓存穿透问题，布隆过滤器解决查询商铺时存在的缓存穿透问题，并使用互斥锁解决用户访问活跃商铺时存在的缓存击穿缓存击穿问题。
- 使用 RabbitMQ 消息队列实现异步处理下单功能；
- 使用 Redis 中 ZSet 数据类型数据类型实现点赞排行榜功能，Set 数据类型数据类型实现好友共同关注功能；
