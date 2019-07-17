# 中华石杉--互联网Java进阶面试训练营

[![original](https://badgen.net/badge/original/%E4%B8%AD%E5%8D%8E%E7%9F%B3%E6%9D%89/orange)]
[![open-source-organization](https://badgen.net/badge/organization/join%20us/138c7b)]
[![reading](https://badgen.net/badge/books/read%20together/cyan)]
[![coding](https://badgen.net/badge/leetcode/coding%20together/cyan)]
[![sharing](https://badgen.net/badge/readers/share%20together/cyan)]
[![stars](https://badgen.net/github/stars/doocs/wulimax/reactApp)]
[![forks](https://badgen.net/github/forks/wulimax/reactApp)]
[![contributors](https://badgen.net/github/contributors/wulimax/reactApp)]
[![help-wanted](https://badgen.net/github/label-issues/wulimax/reactApp/help%20wanted/open)]
[![issues](https://badgen.net/github/open-issues/wulimax/reactApp)]
[![PRs Welcome](https://badgen.net/badge/PRs/welcome/green)](http://makeapullrequest.com)



### 内容说明：
本仓库存放的是公众号【狸猫技术窝】和**中华石杉**老师合作的课程《**互联网Java进阶面试训练营**》的笔记，版权归狸猫技术窝所有，侵权将追究法律责任

训练营详细信息请关注公众号【狸猫技术窝】了解
### 公众号:狸猫技术窝

更多技术干货，请扫描下方二维码，关注公众号狸猫技术窝

![我的公众号](/images/limaojishuwo.jpeg)




## 目录

- [互联网Java面试指南](#面试指南)
    - [备战面试](#备战面试)
    - [常见面试题总结](#常见面试题总结)
    - [面经](#面经)
- [互联网Java面试突击第一季](#面试突击第一季)
    - [分布式消息队列](#分布式消息队列)
    - [分布式搜索引擎](#搜索引擎)
    - [分布式缓存](#分布式缓存)
    - [分库分表](#分库分表)
    - [分布式锁](#分布式锁)
    - [分布式会话](#分布式会话)
    - [分布式事务](#分布式事务)
    - [分布式限流降级](#分布式事务)
    - [分布式服务框架Dubbo](#分布式服务框架Dubbo)
- [互联网Java进阶面试训练营](#互联网Java进阶面试训练营)
    - [第一季:分布式](#第一季-分布式)
    - [第二季:高并发](#第二季-高并发)
    - [第三季:微服务](#第三季-微服务)
    - [第四季:海量数据](#第四季-海量数据)
    - [第五季:高性能](#第五季-高性能)
    - [第六季:高可用](#第六季-高可用)


## 面试指南

### 备战面试
- [面试一线互联网大厂？那这道题目你必须得会！](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484645&idx=1&sn=663238af983603a4c0b33cf42c3ebbcf&chksm=fba6ece6ccd165f0d78f271a21fdc1b91ad8d3def896e2f4df79d9c8d4cf99e3b2978d703dde&mpshare=1&scene=1&srcid=0608edSfhNw7AIjzl9R54Sih%23rd)
- [阿里三面，P9面试官是如何360°无死角考察候选人的？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247485021&idx=1&sn=936b0ecbbe8bd633b1a6c10127eaf4c4&chksm=fba6ee5eccd167483e2a5b17df3f3d1f38f9b98b894f3c47d6b365821338e1380f7c6af1a49d&mpshare=1&scene=1&srcid=0608bZo70WnyWgBMGZs9aAPA%23rd)
- [互联网公司的面试官是如何360°无死角考察候选人的？（上篇）](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484144&idx=1&sn=a6b86d38a762e317ba78e2500fb1a8ff&chksm=fba6eaf3ccd163e5403a01be51216780040511b2ddc4d5750ace6e46b4242ceaf77d0432c680&mpshare=1&scene=1&srcid=0608Ls6BQxXTdAQKvDeZx8f0%23rd)
- [互联网公司面试官是如何360°无死角考察候选人的？（下篇）](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484148&idx=1&sn=a2e05fed6b2dda661b4da11036b883a9&chksm=fba6eaf7ccd163e19013c4204fd0997159b04cd37a235d05dab4f645b61b2f8f9e21a98614c8&mpshare=1&scene=1&srcid=0608k7qLNodHSqW0SbfpZLRG%23rd)
- [中小公司的Java工程师应该如何逆袭冲进BAT？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484442&idx=1&sn=610f02aa18ef6a5d8c80a74959be0333&chksm=fba6ec19ccd1650fc265ac6f7f462157a7b274e358282bb7fc029e9366cfac656c58300b98c5&mpshare=1&scene=1&srcid=06089lyagf3w18D90N7RcB8q%23rd)
- [【offer收割机必备】我简历上的Java项目都好low，怎么办？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484583&idx=1&sn=a9d43c3ee63c8e5a37c073c2b8c43fba&chksm=fba6eca4ccd165b2602a462c5589fa8dacd78558bdee7e0138b02bb26370637714f1094f4e9f&mpshare=1&scene=1&srcid=0608607GubfCXM2YaAqOLXET%23rd)
- [Java工程师如何在1个月内做好面试准备？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484575&idx=1&sn=7075fb3a42ef62fb5e69c868f29c8c61&chksm=fba6ec9cccd1658a391bc4e60faa35b44b947dbb6f535042e392c668693524447a2604955fd8&mpshare=1&scene=1&srcid=0608BvwQetAYtHkxZX7X7r8F%23rd)
### 常见面试题总结
- [互联网大厂Java面试题：使用无界队列的线程池会导致内存飙升吗？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484480&idx=1&sn=1c7262d7f185ad6f99b840fb7779a575&chksm=fba6ec43ccd16555d826772a530c280548d8fd9785a9169b87bb4ed82d8b12ad75154c98b957&mpshare=1&scene=1&srcid=0608DxO0IKPDPxNOoN1la590%23rd)
- [阿里一面：关于【缓存穿透、缓存击穿、缓存雪崩、热点数据失效】问题的解决方案](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484884&idx=1&sn=ceb798b6e8ef0ee608a992385f7d8568&chksm=fba6edd7ccd164c155271811f7948b476955cab41b23f2333847b8c268b31cc9f3332c2e3926&mpshare=1&scene=1&srcid=0608pIX1L8Fja1H99IyorW2X%23rd)
- [大白话聊聊Java并发面试问题之volatile到底是什么？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484058&idx=1&sn=d5c1533204ea655e65947ec57f924799&chksm=fba6ea99ccd1638f945c585cf3b2df6f4d4112b17ea3648730d50fdb5508555d5f30316f4186&mpshare=1&scene=1&srcid=0608cDtcDBaGNgIU9v4zxS3f%23rd)
- [大白话聊聊Java并发面试问题之Java 8如何优化CAS性能?](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484070&idx=1&sn=c1d49bce3c9da7fcc7e057d858e21d69&chksm=fba6eaa5ccd163b3a935303f10a54a38f15f3c8364c7c1d489f0b1aa1b2ef293a35c565d2fda&mpshare=1&scene=1&srcid=0608QzOXG2l0z2QyfVaCKqRH%23rd)
- [大白话聊聊Java并发面试问题之谈谈你对AQS的理解?](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484094&idx=1&sn=b337161f934b1c27ff1f059350ef5e65&chksm=fba6eabdccd163abc8978b65e155d79a133f20ee8a5bff79a33ed20a050c2bd576581db69fe6&mpshare=1&scene=1&srcid=0608yIcfsyrDG1NIBSsF58jq%23rd)
- [大白话聊聊Java并发面试问题之公平锁与非公平锁是啥？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484095&idx=1&sn=aa915ae16d0a550bbe7ae4b6fec99173&chksm=fba6eabcccd163aa2bc0e880d7d3929eee5ff834a73a6ccc3a53237537a4555ef7fd4d9e70d0&mpshare=1&scene=1&srcid=0608QNgPOxWhMZfdNvGvcoUW%23rd)
- [大白话聊聊Java并发面试问题之微服务注册中心的读写锁优化?](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484129&idx=1&sn=d2a95310db5751b152ba070caee4ebae&chksm=fba6eae2ccd163f48aef9d98a4dbb55d578a24af710e1436cc876fe3119b03135532e16d80bc&mpshare=1&scene=1&srcid=06089KYIxoL86LbBEP44hsnV%23rd)
- [消息中间件集群崩溃，如何保证百万生产数据不丢失？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484257&idx=1&sn=e7704f92a1008ab7a292e2826bd079aa&chksm=fba6eb62ccd1627451d439bbc21e46e6fc1d7bfbe2a431fd887cf974a7bd0d9d482697f0e4fd&mpshare=1&scene=1&srcid=0608mcZB6SlZ2JGY46F7giS3%23rd)
- [哥们，消息中间件在你们项目里是如何落地的？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484191&idx=1&sn=fac0c513cf9ad480fc39c5b51f6c4fde&chksm=fba6eb1cccd1620aa0b48c72d1c6b51706400f24268db6c774bac6ec02a0f31885db9b7d6cad&mpshare=1&scene=1&srcid=0608ZI28nnj1eXjYIlBg0oVb%23rd)
- [哥们，那你说说系统架构引入消息中间件有什么缺点？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484157&idx=1&sn=f4644be2db6b1c230846cb4d62ae5be9&chksm=fba6eafeccd163e817b420d57478829d92251a6a5fd446f81805f0983a0d95cb6853a6735c4b&mpshare=1&scene=1&srcid=06083A6RVW3ZtKQRy6Ttq8tK%23rd)
- [哥们，你们的系统架构中为什么要引入消息中间件？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484149&idx=1&sn=98186297335e13ec7222b3fd43cfae5a&chksm=fba6eaf6ccd163e0c2c3086daa725de224a97814d31e7b3f62dd3ec763b4abbb0689cc7565b0&mpshare=1&scene=1&srcid=0608fz8HKZvYxRhzFqyJ4Isq%23rd)
- [线上服务宕机时，如何保证数据100%不丢失?](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484204&idx=1&sn=6fc43b0620857b653dbef20693d1c6c6&chksm=fba6eb2fccd16239056e4b52dc0895585292b830bfd2652dea81b7360556fe36aceac0951761&mpshare=1&scene=1&srcid=0608W9lqShQsPrfETC90Acwm%23rd)


### 面经
- [小公司面试10连挂之后，我拿到了互联网一线大厂offer！](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484955&idx=1&sn=be39f51e00d78eb7d3a4ae6b7137e62c&chksm=fba6ee18ccd1670ec7dbf62f2c73d65b241cfb6897bac9316981c1e7936e31c1caee5ccee87e&mpshare=1&scene=1&srcid=0608zdpqBAGKWQr6ExuWOvtg%23rd)
- [尴尬的面试现场：说说你们系统有多大QPS？系统到底怎么抗住高并发的？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484908&idx=1&sn=6acc6ff3ce5e2ca1d0c2639868356a5e&chksm=fba6edefccd164f92d15faab6b8f77e4118c299ea5b1c366ac2db2aad9f12c761ef051355600&mpshare=1&scene=1&srcid=0608rMH6pNVzMB7wHy5caCrN%23rd)
- [面对BAT大厂的竞争对手时，小公司Java工程师是如何败北的？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484786&idx=1&sn=be07d63f36ee97031031dc455c03e3ca&chksm=fba6ed71ccd164677ef4e94ad64409783ec4a35d0cf8cfc2f2672a58099a382a496db2abf313&mpshare=1&scene=1&srcid=0608FUyrpWhHO2WyA36i9JK9%23rd)
- [我一连面试了十个Java岗，统统石沉大海！](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484590&idx=1&sn=9d63dd0c4ab9150f6ac32f327d349d3b&chksm=fba6ecadccd165bb3c96ebd792d677ce25614f1cf48dbbe255534c149fe447c88761077f16b4&mpshare=1&scene=1&srcid=0608MowbddtGYWq6Fa26nPIJ%23rd)
- [面试最让你手足无措的一个问题：你的系统如何支撑高并发？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484429&idx=1&sn=d8038c21ecd733b8bb7ff784014243f9&chksm=fba6ec0eccd165189e92a294ab2b7cd6796982c188befe05c27f4e96ae5cd39f2baf436cf37d&mpshare=1&scene=1&srcid=0608ttwG3fBdBUt7pdxL5IhX%23rd)
- [【斩获7枚offer，入职阿里平台事业部】横扫阿里、美团、京东、 去哪儿之后，我写下了这篇面经！](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247485090&idx=1&sn=5502672d9bf52551038b911d7ab623b9&chksm=fba6eea1ccd167b73a542b76dad423da21a2b452f768aac996cb50eeac1adc5d4978afe762ce&mpshare=1&scene=1&srcid=0608mo3eKwh686hXNzvRQfEB%23rd)
- [三年努力，梦归阿里！](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247485010&idx=1&sn=cd158d8358a0758fa81af094d58e2ea2&chksm=fba6ee51ccd1674753d77c8ab2a522cd8e32373b0a104eb9ecd6008cd12b6457eaade77e0514&mpshare=1&scene=1&srcid=0608LIOSiYzoUmlBHC4ZhnnZ%23rd)
- [二本出身、逆袭网易、一路孤独、一路狂欢！](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484844&idx=1&sn=cfa78df2943567269909f87217fa25c8&chksm=fba6edafccd164b9f6c22162a6386734010aeee9a084de720dacbb72d58bd1c20c0f961f5315&mpshare=1&scene=1&srcid=0608Ufv5zYZu66XnNn89WYEU%23rd)
- [小公司出身的我，是如何拿下知名独角兽公司offer的？](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484813&idx=1&sn=4c9a43e51e1cf114efcf938e60ad58fd&chksm=fba6ed8eccd16498840a715659b8a29cf3368d28cf67c6fb27255277abe63421bca9ceb2cae7&mpshare=1&scene=1&srcid=06083zOsdotiVg1juwK3MYxZ%23rd)
- [【行走的Offer收割机】记一位朋友斩获BAT技术专家Offer的面试经历](https://mp.weixin.qq.com/s?__biz=MzU0OTk3ODQ3Ng==&mid=2247484170&idx=1&sn=6c178884c1c5399e37562b9dc66cff6c&chksm=fba6eb09ccd1621ff8821b37f12d6df8a1d269ddc95ad10c0a4e71a3bf0017952bf19978d8ec&mpshare=1&scene=1&srcid=0608ezj6dEIln43Sl011MZz3%23rd)    
    



## 面试突击第一季

### [分布式消息队列](/docs/high-concurrency/mq-interview.md)
- [为什么使用消息队列？消息队列有什么优点和缺点？Kafka、ActiveMQ、RabbitMQ、RocketMQ 都有什么优点和缺点？](/docs/high-concurrency/why-mq.md)
- [如何保证消息队列的高可用？](/docs/high-concurrency/how-to-ensure-high-availability-of-message-queues.md)
- [如何保证消息不被重复消费？（如何保证消息消费的幂等性）](/docs/high-concurrency/how-to-ensure-that-messages-are-not-repeatedly-consumed.md)
- [如何保证消息的可靠性传输？（如何处理消息丢失的问题）](/docs/high-concurrency/how-to-ensure-the-reliable-transmission-of-messages.md)
- [如何保证消息的顺序性？](/docs/high-concurrency/how-to-ensure-the-order-of-messages.md)
- [如何解决消息队列的延时以及过期失效问题？消息队列满了以后该怎么处理？有几百万消息持续积压几小时，说说怎么解决？](/docs/high-concurrency/mq-time-delay-and-expired-failure.md)
- [如果让你写一个消息队列，该如何进行架构设计啊？说一下你的思路。](/docs/high-concurrency/mq-design.md)

### 搜索引擎
- [lucene 和 es 的前世今生](/docs/high-concurrency/es-introduction.md)
- [es 的分布式架构原理能说一下么（es 是如何实现分布式的啊）？](/docs/high-concurrency/es-architecture.md)
- [es 写入数据的工作原理是什么啊？es 查询数据的工作原理是什么啊？底层的 lucene 介绍一下呗？倒排索引了解吗？](/docs/high-concurrency/es-write-query-search.md)
- [es 在数据量很大的情况下（数十亿级别）如何提高查询效率啊？](/docs/high-concurrency/es-optimizing-query-performance.md)
- [es 生产集群的部署架构是什么？每个索引的数据量大概有多少？每个索引大概有多少个分片？](/docs/high-concurrency/es-production-cluster.md)

### 分布式缓存
- [在项目中缓存是如何使用的？缓存如果使用不当会造成什么后果？](/docs/high-concurrency/why-cache.md)
- [Redis 和 Memcached 有什么区别？Redis 的线程模型是什么？为什么单线程的 Redis 比多线程的 Memcached 效率要高得多？](/docs/high-concurrency/redis-single-thread-model.md)
- [Redis 都有哪些数据类型？分别在哪些场景下使用比较合适？](/docs/high-concurrency/redis-data-types.md)
- [Redis 的过期策略都有哪些？手写一下 LRU 代码实现？](/docs/high-concurrency/redis-expiration-policies-and-lru.md)
- [如何保证 Redis 高并发、高可用？Redis 的主从复制原理能介绍一下么？Redis 的哨兵原理能介绍一下么？](/docs/high-concurrency/how-to-ensure-high-concurrency-and-high-availability-of-redis.md)
- [Redis 的持久化有哪几种方式？不同的持久化机制都有什么优缺点？持久化机制具体底层是如何实现的？](/docs/high-concurrency/redis-persistence.md)
- [Redis 集群模式的工作原理能说一下么？在集群模式下，Redis 的 key 是如何寻址的？分布式寻址都有哪些算法？了解一致性 hash 算法吗？如何动态增加和删除一个节点？](/docs/high-concurrency/redis-cluster.md)
- [了解什么是 redis 的雪崩、穿透和击穿？Redis 崩溃之后会怎么样？系统该如何应对这种情况？如何处理 Redis 的穿透？](/docs/high-concurrency/redis-caching-avalanche-and-caching-penetration.md)
- [如何保证缓存与数据库的双写一致性？](/docs/high-concurrency/redis-consistence.md)
- [Redis 的并发竞争问题是什么？如何解决这个问题？了解 Redis 事务的 CAS 方案吗？](/docs/high-concurrency/redis-cas.md)
- [生产环境中的 Redis 是怎么部署的？](/docs/high-concurrency/redis-production-environment.md)

### 分库分表
- [为什么要分库分表（设计高并发系统的时候，数据库层面该如何设计）？用过哪些分库分表中间件？不同的分库分表中间件都有什么优点和缺点？你们具体是如何对数据库如何进行垂直拆分或水平拆分的？](/docs/high-concurrency/database-shard.md)
- [现在有一个未分库分表的系统，未来要分库分表，如何设计才可以让系统从未分库分表动态切换到分库分表上？](/docs/high-concurrency/database-shard-method.md)
- [如何设计可以动态扩容缩容的分库分表方案？](/docs/high-concurrency/database-shard-dynamic-expand.md)
- [分库分表之后，id 主键如何处理？](/docs/high-concurrency/database-shard-global-id-generate.md)
- [如何实现 MySQL 的读写分离？MySQL 主从复制原理是啥？如何解决 MySQL 主从同步的延时问题？](/docs/high-concurrency/mysql-read-write-separation.md)


### 分布式服务框架Dubbo
- [面试连环炮](/docs/distributed-system/distributed-system-interview.md)
- [如何设计一个高并发系统？](/docs/high-concurrency/high-concurrency-design.md)
- [说一下 Dubbo 的工作原理？注册中心挂了可以继续通信吗？](/docs/distributed-system/dubbo-operating-principle.md)
- [Dubbo 支持哪些序列化协议？说一下 Hessian 的数据结构？PB 知道吗？为什么 PB 的效率是最高的？](/docs/distributed-system/dubbo-serialization-protocol.md)
- [Dubbo 负载均衡策略和集群容错策略都有哪些？动态代理策略呢？](/docs/distributed-system/dubbo-load-balancing.md)
- [Dubbo 的 spi 思想是什么？](/docs/distributed-system/dubbo-spi.md)
- [如何基于 Dubbo 进行服务治理、服务降级、失败重试以及超时重试？](/docs/distributed-system/dubbo-service-management.md)
- [分布式服务接口的幂等性如何设计（比如不能重复扣款）？](/docs/distributed-system/distributed-system-idempotency.md)
- [分布式服务接口请求的顺序性如何保证？](/docs/distributed-system/distributed-system-request-sequence.md)
- [如何自己设计一个类似 Dubbo 的 RPC 框架？](/docs/distributed-system/dubbo-rpc-design.md)
- [为什么要进行系统拆分？如何进行系统拆分？拆分后不用 Dubbo 可以吗？](/docs/distributed-system/why-dubbo.md)


### 分布式锁
- [Zookeeper 都有哪些应用场景？](/docs/distributed-system/zookeeper-application-scenarios.md)
- [使用 Redis 如何设计分布式锁？使用 Zookeeper 来设计分布式锁可以吗？以上两种分布式锁的实现方式哪种效率比较高？](/docs/distributed-system/distributed-lock-redis-vs-zookeeper.md)

### 分布式事务
- [分布式事务了解吗？你们如何解决分布式事务问题的？TCC 如果出现网络连不通怎么办？XA 的一致性如何保证？](/docs/distributed-system/distributed-transaction.md)

### 分布式会话
- [集群部署时的分布式 Session 如何实现？](/docs/distributed-system/distributed-session.md)

## 分布式限流降级
- [Hystrix 介绍](/docs/high-availability/hystrix-introduction.md)
- [电商网站详情页系统架构](/docs/high-availability/e-commerce-website-detail-page-architecture.md)
- [Hystrix 线程池技术实现资源隔离](/docs/high-availability/hystrix-thread-pool-isolation.md)
- [Hystrix 信号量机制实现资源隔离](/docs/high-availability/hystrix-semphore-isolation.md)
- [Hystrix 隔离策略细粒度控制](/docs/high-availability/hystrix-execution-isolation.md)
- [深入 Hystrix 执行时内部原理](/docs/high-availability/hystrix-process.md)
- [基于 request cache 请求缓存技术优化批量商品数据查询接口](/docs/high-availability/hystrix-request-cache.md)
- [基于本地缓存的 fallback 降级机制](/docs/high-availability/hystrix-fallback.md)
- [深入 Hystrix 断路器执行原理](/docs/high-availability/hystrix-circuit-breaker.md)
- [深入 Hystrix 线程池隔离与接口限流](/docs/high-availability/hystrix-thread-pool-current-limiting.md)
- [基于 timeout 机制为服务接口调用超时提供安全保护](/docs/high-availability/hystrix-timeout.md)



## 互联网Java进阶面试训练营

### 第一季-分布式
### 第二季-高并发
### 第三季-微服务
### 第四季-海量数据
### 第五季-高性能
### 第六季-高可用











