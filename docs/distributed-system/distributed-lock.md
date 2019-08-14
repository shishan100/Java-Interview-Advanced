
下订单的环节，支付之前，创建一个订单

![distributed-lock](/docs/distributed-system/images/distributed-lock.png)
创建一个订单，订单里会指定对哪些商品要购买多少件，此时就需要走一个流程，校验一下库存

查库存，确认库存充足，锁定库存

这个过程必须用分布式锁，锁掉这个商品的库存，对一个商品的购买同一时间只能有一个人操作

redis和zookeeper实现分布式锁的原理，在之前面试突击第一季都讲过了，大家没看过的可以去看一下
