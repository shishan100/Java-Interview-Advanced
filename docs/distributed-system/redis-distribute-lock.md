
面试突击第二季
![distributed-lock](/docs/distributed-system/images/redis-distribute-lock.png)
Redis分布式锁，很少自己撸，Redisson框架，他基于Redis实现了一系列的开箱即用的高级功能，比如说分布式锁

引入maven依赖，他示例代码就几行

比如说，苹果这个商品的id是1

redisson.lock(“product_1_stock”)

key的业务语义，就是针对product_id = 1的商品的库存，也就就是苹果的库存，进行加锁

如果要学习redis技术的，跟我之前录制的《亿级流量商品详情页系统》去学习，在训练营的课程目录里有一个文档，有我之前的课程的地址


product_1_stock: {
“xxxx”: 1
}

生存时间：30s

watchdog，redisson框架后台执行一段逻辑，每隔10s去检查一下这个锁是否还被当前客户端持有，如果是的话，重新刷新一下key的生存时间为30s

其他客户端尝试加锁，这个时候发现“product_1_stock”这个key已经存在了，里面显示被别的客户端加锁了，此时他就会陷入一个无限循环，阻塞住自己，不能干任何事情，必须在这里等待


第一个客户端加锁成功了，此时有两种情况，第一种情况，这个客户端操作完毕之后，主动释放锁；第二种情况，如果这个客户端宕机了，那么这个客户端的redisson框架之前启动的后台watchdog线程，就没了

此时最多30s，key-value就消失了，自动释放了宕机客户端之前持有的锁






