### 1.项目概述
此项目为厦门大学信息学院软测测试课程测试系统

 ### 2.技术栈
> 后台管理端和前台移动端主要使用SpringBoot+Mybatis-Plus实现数据库的CRUD操作,项目中的图片上传与下载采用七牛云,数据缓存使用Redis,共二种方式 Spring Data Redis和SpringCache,垃圾清理端主要采用Spring+MyBatis实现数据的查询与删除操作,采用Quartz定时组件实现每周星期天晚上23点清理数据库中的垃圾数据(被后台管理端删除后的数据,采用了逻辑删除),每日晚23点清理Redis缓存数据(用于记录七牛云中所有上传图片和上传到数据库中图片的数据)和七牛云中的垃圾数据。
> 
> 相关知识点如下: 
> ① SpringBoot和Spring
> ② MyBatis 和 Mybatis-Plus
> ③ Redis
> ④ Spring Data Redis和SpringCache
> ⑤ Mysql
> ⑥ Quartz定时组件
> ⑦ 七牛云

### 2.软件预览
#### (1) 后台管理端

> 后台管理端访问路径为:[http://localhost:8089/backend/page/login/login.html](账号admin,密码:123456)
 

 - 后台登入


![在这里插入图片描述](http://ruw4252pn.hn-bkt.clouddn.com/login.png)

 - 员工管理

![在这里插入图片描述](http://ruw4252pn.hn-bkt.clouddn.com/member.png)

 - 分类管理

![在这里插入图片描述](http://ruw4252pn.hn-bkt.clouddn.com/fenlei.png)

- 菜品管理

![在这里插入图片描述](http://ruw4252pn.hn-bkt.clouddn.com/dish.png)

- 套餐管理

![在这里插入图片描述](http://ruw4252pn.hn-bkt.clouddn.com/taocan.png)

- 订单详情

![在这里插入图片描述](http://ruw4252pn.hn-bkt.clouddn.com/order.png)
#### (2) 前台移动端

> 访问路径: [http://localhost:8089/front/page/login.html]
> 
![在这里插入图片描述](http://ruw4252pn.hn-bkt.clouddn.com/phone.png)



