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

后台管理端:

![在这里插入图片描述](https://img-blog.csdnimg.cn/faa23574c4cc432db12aae0bf8621805.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/00976a03710540549930ab98a3532c66.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/a7c2618716d94de3bbe6b6a56a9bc1bf.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/5dc982a8f97347189aa1fceb38e044ce.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/a023b95d5d8f4372b054ab26bfe386e0.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/c907c5be23414a4690847e0cb1b96752.png)

前台移动端:
![在这里插入图片描述](https://img-blog.csdnimg.cn/28f659c8e6e345899232a767506dad28.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/909a798e54b54692bca040d0bcdffe54.png)


### 5.软件预览
#### (1) 后台管理端

> 后台管理端访问路径为:[http://124.220.28.236:8089/backend/page/login/login.html](http://124.220.28.236:8089/backend/page/login/login.html)(账号zhangsan,密码:123456)
 

 - 后台登入


![在这里插入图片描述](https://img-blog.csdnimg.cn/ddc6805525f74da182c776b411ac8748.png)

 - 员工管理

![在这里插入图片描述](https://img-blog.csdnimg.cn/8a643ebdad6d4a729e94576e7b6ebf1c.png)

 - 分类管理

![在这里插入图片描述](https://img-blog.csdnimg.cn/443742e14c45427e9adacecbe69deadd.png)

- 菜品管理(批量处理业务视频中未编写,这里我编写了的)

![在这里插入图片描述](https://img-blog.csdnimg.cn/bcfa2db9f9794fb8b7c162dd2ed5f8f7.png)

- 套餐管理(批量处理业务视频中未编写,这里我编写了)

![在这里插入图片描述](https://img-blog.csdnimg.cn/886dea1f6b2a4a02aeb67c3cc4cad5c7.png)

- 订单详情(视频中该本分业务未编写,这里我编写了)

![在这里插入图片描述](https://img-blog.csdnimg.cn/88aafab8bfa54da396c05070b6be9a84.png)
#### (2) 前台移动端

> 游览器访问需要手机适配设置(按F12适配手机),访问路径: [http://124.220.28.236:8089/front/page/login.html](http://124.220.28.236:8089/front/page/login.html)（手机号:13812345678,点击获取验证码,进行登入即可）
> 
![在这里插入图片描述](https://img-blog.csdnimg.cn/f3bd136ab1a14f8b9f273f8bafbd6ea1.png)

- 登入页面

![在这里插入图片描述](https://img-blog.csdnimg.cn/72375f2a998e4c3f8750e60a66211f4d.png)

- 服务大厅

![在这里插入图片描述](https://img-blog.csdnimg.cn/2cfc7458eb02458fa23a2b2a23d978ed.png)

- 订单结算页面

![在这里插入图片描述](https://img-blog.csdnimg.cn/3cda66d0cf53483da4017074138b43a4.png)

- 个人中心

![在这里插入图片描述](https://img-blog.csdnimg.cn/ac3fd526ef3a4c4ebbc5b9b7ff7d5d29.png)

- 地址管理

![在这里插入图片描述](https://img-blog.csdnimg.cn/83f3c621063c4c6abea3b4b30dfc7968.png)

- 历史订单

![在这里插入图片描述](https://img-blog.csdnimg.cn/f08b317dd8444e7d818422ba323097c3.png)

清理Redis中的缓存和七牛云的垃圾数据:

![在这里插入图片描述](https://img-blog.csdnimg.cn/1dfbda3ddc744724ba87ce01b0fbf2de.png)

清理数据库和七牛云中的垃圾数据:

![在这里插入图片描述](https://img-blog.csdnimg.cn/3a18b1d8404141a9bfd36f85af8f9658.png)
