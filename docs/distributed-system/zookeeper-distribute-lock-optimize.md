
![zookeeper-distribute-lock-optimize](/docs/distributed-system/images/zookeeper-distribute-lock-optimize.png)
也可以，羊群效应

如果几十个客户端同时争抢一个锁，此时会导致任何一个客户端释放锁的时候，zk反向通知几十个客户端，几十个客户端又要发送请求到zk去尝试创建锁，所以大家会发现，几十个人要加锁，大家乱糟糟的，无序的

羊群效应

造成很多没必要的请求和网络开销，会加重网络的负载



