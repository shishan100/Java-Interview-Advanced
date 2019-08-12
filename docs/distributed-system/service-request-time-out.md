
分布式系统，拆分为很多个服务之后，他们互相之间要进行调用，平时服务内要优化的一些参数其实不多，服务与服务之间的调用，会不会出现调用的超时，每个服务超时的时间是多长，超时之后是否要进行重试，重试几次

高可用，hystrix进行资源隔离、熔断、降级，zuul网关层直接进行限流


网关 ->（卡住） 订单服务 ->（卡住） wms服务

网关收到的一个http响应，可能就是一个500，internal error





Spring Cloud生产优化，系统第一次启动的时候，人家调用你经常会出现timeout

每个服务第一次被请求的时候，他会去初始化一个Ribbon的组件，初始化这些组件需要耗费一定的时间，所以很容易会导致。让每个服务启动的时候就直接初始化Ribbon相关的组件，避免第一次请求的时候初始化

```
ribbon:
  eager-load:
    enabled: true


zuul:
  ribbon:
    eager-load:
      enabled: true

feign:
  hystrix:
enabled: false

```

我们刚才启动了wms服务之后，其实订单服务和积分服务、wms服务、库存服务之间的请求都是没问题的，日志全部都打印出来了，不会说第一次请求因为ribbon加载过慢导致请求失败的问题

但是zuul网关层面去请求订单服务的时候，他还是可能会认为自己超时了，windows电脑上跑这样的一套系统，网络请求都是比较慢的，因为你有很多服务与服务之间的调用，order和另外3个服务一套交互下来，比如超过了1秒钟

zuul而言感觉耗时太久了，还是会认为是超时的

windows电脑走的都是家用网络，我家里的网络情况不是太好，网卡，网速慢，信号弱




线上的服务，每个服务部署上线的时候，一般来说都需要配置相关的超时时间还有重试次数

订单服务 -> 积分服务、库存服务、仓促服务

订单服务对于其他服务的调用，一般来说限制在多长时间就必须认为是超时了，如果超时之后如何进行重试

积分服务部署了两台机器，机器1和机器2

订单服务在一次请求积分服务的机器1的时候，超过1秒钟，超时了；此时需要进行重试，对积分服务当前的这台机器1重试几次？如果说机器1不行，是否可以重试一下积分服务的机器2？


```
ribbon:
  ConnectTimeout: 3000
  ReadTimeout: 3000
  OkToRetryOnAllOperations: true
  MaxAutoRetries: 1
  MaxAutoRetriesNextServer: 1

中小型的系统，没必要直接开启hystrix，资源隔离、熔断、降级，如果你没有设计好一整套系统高可用的方案

zuul请求一个订单服务，超过1秒就认为超时了，此时会先重试一下订单服务这台机器，如果还是不行就重试一下订单服务的其他机器

<dependency>
<groupId>org.springframework.retry</groupId>
<artifactId>spring-retry</artifactId>
</dependency>

hystrix.command.default.execution.isolation.thread.timeoutInMilliseconds=10000
```