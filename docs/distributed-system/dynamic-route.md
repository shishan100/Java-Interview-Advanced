```
CREATE TABLE `gateway_api_route` (
   `id` varchar(50) NOT NULL,
   `path` varchar(255) NOT NULL,
   `service_id` varchar(50) DEFAULT NULL,
   `url` varchar(255) DEFAULT NULL,
   `retryable` tinyint(1) DEFAULT NULL,
   `enabled` tinyint(1) NOT NULL,
   `strip_prefix` int(11) DEFAULT NULL,
   `api_name` varchar(255) DEFAULT NULL,
   PRIMARY KEY (`id`)
 ) ENGINE=InnoDB DEFAULT CHARSET=utf8

INSERT INTO gateway_api_route (id, path, service_id, retryable, strip_prefix, url, enabled) VALUES ('order-service', '/order/**', 'order-service',0,1, NULL, 1);

   ```

你可以自己用简单的spring mvc+前端页面封装一个可视化的网关管理工作台，如果新开发了一个服务之后，就可以在这个界面上配置一下，说某个服务对应某个url路径，修改，增删改查

http://localhost:9000/order/order/create?productId=1&userId=1&count=2&totalPrice=50

生产级，企业级的功能，网关的动态路由
