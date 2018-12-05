# 学习
> 包含功能如下

- 1. 控制台输出完整sql语句(即 ?变 真实值)  
- 2. 预计下一版本出现


# 如何使用
## springmvc-方式
> 1、maven 依赖  (已提交到阿里云镜像库)
```
		<dependency>
			<groupId>org.kd</groupId>
			<artifactId>mybatis-tool-box</artifactId>
			<version>1.0-M10</version>
		</dependency>
```

> 2、在 mybatis mybatisConfig.xml 添加
```
	<plugins> 
		<!-- 打印完整sql语句   mysad -->
		<plugin interceptor="org.kd.intercepts.MybatisAutoSql" />
	</plugins>  
```


## springboot方式


> 1、只需依赖spring-boot-starter启动器即可 
```
		<dependency>
	        <groupId>showSql-spring-boot-starter</groupId>
	        <artifactId>showSql-spring-boot-starter</artifactId>
	        <version>1.0-M1</version>
		</dependency>

```

## 测试
> 3、测试 -控制台输出-(mysql)
```
========================================================
https://github.com/open-plans
========================================================
执行XML方法:org.kd.dao.UserDao.queryUserForLogin
执行的完整的sql语句-------------------mysad
SELECT id,name,pwd,user_name,age,birthday,add_time,head_img,create_time,update_time,del_flag 
from user where name='kd' and pwd='123456'
执行的sql语句的时间:330ms
```		