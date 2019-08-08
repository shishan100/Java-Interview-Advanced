
#### 准备一个数据库和一个表（也可以用Apollo配置中心、Redis、ZooKeeper，其实都可以），放一个灰度发布启用表

```
id service_id path enable_gray_release

CREATE TABLE `gray_release_config` (
   `id` int(11) NOT NULL AUTO_INCREMENT,
   `service_id` varchar(255) DEFAULT NULL,
   `path` varchar(255) DEFAULT NULL,
   `enable_gray_release` int(11) DEFAULT NULL,
   PRIMARY KEY (`id`)
 ) ENGINE=InnoDB DEFAULT CHARSET=utf8
 


在zuul里面加入下面的filter，可以在zuul的filter里定制ribbon的负载均衡策略

<dependency>
			<groupId>io.jmnarloch</groupId>
			<artifactId>ribbon-discovery-filter-spring-cloud-starter</artifactId>
			<version>2.1.0</version>
		</dependency>

写一个zuul的filter，对每个请求，zuul都会调用这个filter

@Configuration
public class GrayReleaseFilter extends ZuulFilter {

@Autowired
private JdbcTemplate jdbcTemplate;

    @Override
    public int filterOrder() {
        return PRE_DECORATION_FILTER_ORDER - 1;
    }
 
    @Override
    public String filterType() {
        return PRE_TYPE;
    }
 
    @Override
    public boolean shouldFilter() {
    	
    }
 
    @Override
    public Object run() {
        RequestContext ctx = RequestContext.getCurrentContext();
        HttpServletRequest request = ctx.getRequest();

Random random = new Random();
int seed = random.getInt() * 100;

        if (seed = 50) {
            // put the serviceId in `RequestContext`
            RibbonFilterContextHolder.getCurrentContext()
                    .add("version", "new");
        }  else {
            RibbonFilterContextHolder.getCurrentContext()
                    .add("version", "old");
        }
        
        return null;
    }
}
 ```

eureka:
instance:
metadata-map:
version: new



