# 它基于Laravel 5.7 开发的一个小小的电商平台，可以用于新手学习参考

# 请注意，改项目已经停止维护 ！！！！，仅供参考

欢迎加入微信群: 

![WechatIMG18.jpeg](https://surest.cn/usr/uploads/2021/03/2515408408.jpeg)

这里先感谢laravel提供了一个好的平台、包括路上教导的助教，十分感谢你们的答疑~！！！

![](https://cdn.pixabay.com/photo/2018/10/04/14/22/donut-3723751_960_720.jpg)


-----------------

![file](https://iocaffcdn.phphub.org/uploads/images/201811/26/26353/OSLz88Czsb.png!/fw/1240)

![file](https://iocaffcdn.phphub.org/uploads/images/201811/26/26353/B2yxunoaYM.png!/fw/1240)

![file](https://iocaffcdn.phphub.org/uploads/images/201811/26/26353/PqbY3MA2r5.png!/fw/1240)


功能如下： 

- 活跃用户列表
- 支持QQ、微博、微信(仿微信登陆)
- 发送订阅信息
- 支付宝、微信支付
- 商品列表推荐
- 购物车模块、收藏模块、订单、收获地址等
- 在 linux  服务器上设置cron定时发送咨询信息、清除相关缓存
- 后台管理用户与会员用户分离
- 合理设置了mysql索引、外键
- 基本常见的使用页面采用了redis保存，页面访问速度极快
 
 ## 使用的扩展包

- monolog 

- GuzzleHttp

- new/captcha

- spatie/laravel-permission

- zgldh/qiniu-laravel-storage

- predis

- yansongda/pay

- endroid/qr-code

- emadadly/laravel-uuid


##  安装：
 ```
git clone git@github.com:RA31/shop_surest.git
 
cp .env.example .env   

composer update 


# 创建数据库
mysql

create database m_shop
exit

------
# 安装
 php artisan install:init
```
 
 ##  以上采用的是homestead环境部署
 
> 第一次开源自己写的东西，不足之处请谅解，包括代码可能杂乱，稳定不清晰等，谢谢~~

感谢大佬 [[[@DavidNineRoc](https://laravel-china.org/users/17682)](https://laravel-china.org/users/17682)](https://laravel-china.org/users/17682) 提供的静态模板

 [演示地址：](http://shop.surest.cn)  
 [后台管理：](http://shop.surest.cn/admin)
 [github地址](https://github.com/RA31/shop_surest)
 
 希望能给个star  -_-
  
后台账号密码： admin / admin 

 # 页面错误修改
 
 - 当删除分类后商品链接到分类id的时候回报错 no-object ， 已修改
 
 - 后台分类添加的时候，添加异常， 可查看storage\log\sys文件
 
 - 使用 模型观察期在 删除分类数据的时候同时删除 分类相关信息
 
 - 修改日志记录为daily 级别为 error And 关闭显示demo的调试模式
 
 - 修复和分类数据和首页数据不一致的情况
 
 - 修复了分类数据在 0 条数据的情况下不应该显示的问题
 
 - 为了安全考虑， 删除了.envample中的私密信息，请自我校对
