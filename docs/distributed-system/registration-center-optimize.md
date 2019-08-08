
![分布式注册中心](/docs/distributed-system/images/registration-center-optimize.png)
#### eureka：peer-to-peer，每台机器都是高并发请求，有瓶颈
#### zookeeper：服务上下线，全量通知其他服务，网络带宽被打满，有瓶颈

#### 分布式服务注册中心，分片存储服务注册表，横向扩容，每台机器均摊高并发请求，各个服务主动拉取，避免反向通知网卡被打满
