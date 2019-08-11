

训练营的课程目录里，有我之前的一些课程，在网上大家都可以去看

亿级流量电商详情页系统
elasticsearch从入门到精通

针对某个技术领域手把手的教学，课程内容量非常的大，代码都是一行一行的写


https://github.com/seata/seata


自己安装一个git bash，百度一下如何安装即可，在win上可以执行linux类的命令

然后自己建一个目录

git clone https://github.com/seata/seata-samples.git

也可以直接在github页面上下载：https://github.com/seata/seata-samples，建议这种方式，比较快一点，git clone速度太慢了

就可以把seata所有的示例代码拷贝下来，里面提供的例子就是跟我们说的电商的核心例子是类似的，然后导入到Eclipse中去，这个过程会eclipse会通过maven下载很多的依赖，需要耐心等待

使用脚本初始化数据库

```
CREATE TABLE `account_tbl` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `user_id` varchar(255) DEFAULT NULL,
  `money` int(11) DEFAULT '0',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8;

CREATE TABLE `storage_tbl` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `commodity_code` varchar(255) DEFAULT NULL,
  `count` int(11) DEFAULT '0',
  PRIMARY KEY (`id`),
  UNIQUE KEY `commodity_code` (`commodity_code`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8;

CREATE TABLE `order_tbl` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `user_id` varchar(255) DEFAULT NULL,
  `commodity_code` varchar(255) DEFAULT NULL,
  `count` int(11) DEFAULT '0',
  `money` int(11) DEFAULT '0',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8;

CREATE TABLE `undo_log` (
  `id` bigint(20) NOT NULL AUTO_INCREMENT,
  `branch_id` bigint(20) NOT NULL,
  `xid` varchar(100) NOT NULL,
  `context` varchar(128) NOT NULL,
  `rollback_info` longblob NOT NULL,
  `log_status` int(11) NOT NULL,
  `log_created` datetime NOT NULL,
  `log_modified` datetime NOT NULL,
  `ext` varchar(100) DEFAULT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `ux_undo_log` (`xid`,`branch_id`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8;
```
然后先要下载一个seata-server到本地，在这里下载：https://github.com/seata/seata/releases，然后启动起来，这是分布式事务管理中心，负责维护每一个分布式事务的状态，触发分布式事务的提交和回滚

seata-server.bat -h 127.0.0.1 -p 8091 -m file

直接把Spring Cloud版本的例子运行起来，观察一下依赖、配置和代码，以后自己在系统里使用直接仿照即可，eureka、account、order、storage、business，依次运行起来，修改一些配置，比如说数据库连接配置


但是任何一个服务报错之后，seata这个分布式事务的框架会感知到，自动触发所有服务之前做的数据库操作全部进行回滚


纯正的tcc框架，很麻烦，需要你手动把各种接口实现出来3个接口，try，confirm，cancel，bytetcc，纯的tcc框架，star






