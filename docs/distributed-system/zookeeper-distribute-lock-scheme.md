
Redis和ZooKeeper，哪种分布式锁更好？

从分布式系统协调语义而言，是ZooKeeper做分布式锁更好一些，因为Redis本身其实是缓存，但是Redis能抗高并发，高并发场景下更好一些

zookeeper本身不适合部署大规模集群，他本身适用的场景就是部署三五台机器，不是承载高并发请求的，仅仅是用作分布式系统的协调的


Redis？ZooKeeper？

有redis集群，没有zookeeper集群，那你当然就选择redis了；如果你们公司两个都有，用哪种分布式锁都可以，高并发场景，redis
