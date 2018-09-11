# 前言

#### 介绍
Regan API 项目是基于注释自动生成api文档，很大缩短了开始与后期维护API接口文档的时间。 Regan API 利用jdk提供的Doclet 类读取文档注释，可手动配置需要读取的文件，同时增加了读取过滤指定方法过滤等功能。

Regan API 是在开发中突发奇想的一个项目，对程序猿来说难的并不是开发一个项目，最难的反而是不断变更的需求与后期文档混乱不清以至于自己都懒得再去维护，遇到问题了还得一遍遍去读自己甚至别人的代码。于是想可否结合起来，直接去读取注释然后生成APi文档。网上也搜索了许多类似的项目，后来发觉我并不是第一个有这个想法的人。 同样结合了别人的代码，最后发现原理都差不多，于是有了想法就开始了实践。刚好在开发这个项目的期间，自己在学习react,于是就把这两个结合了。

?> Regan API 最初的版本是基于[jfinal](http://www.jfinal.com/)与React的ui框架[飞冰](https://alibaba.github.io/ice)开发的，后续增加了Springboot版本。代码很简单，只需要引入几个API文件，与html文件即可。

#### 版本
  - Jfinal: [https://github.com/zhangbiy/jfinal-api](https://github.com/zhangbiy/jfinal-api)
  - springboot: [https://github.com/zhangbiy/regan_api](https://github.com/zhangbiy/regan_api)
#### java源码
``` java
/**
 * 用户管理
 * @action /user
 * @author zhangby
 * @date 2018/6/12 下午3:26
 */
public class UserController extends Controller {
    /**
     * 用户登录功
     * @title 登录接口
     * @param username|用户名|string|必填
     * @param password|密码|string|必填
     * @resqParam code|用户名|String|必填
     * @resqParam data|数据|object|非必填
     * @resqParam msg|消息信息|String|必填
     * @respBody {"code":"000","data":"","msg":"success"}
     * @requestType post,get
     * @author zhangby
     * @date 2018/6/12 下午4:23
     */
    public void login() {
        renderJson(Kv.create().set("code","000"));
    }
}
```
#### 截图
_**dark主题**_

![](http://file.homeins.cn/FjnP0FvBDFwKRH4LLFwzYyI_tvbH)
![](http://file.homeins.cn/FrIAtiOVuYau1WLQ33M3w4Sqj4q5)

_**lighit主题**_

![](https://regan_jeff.gitee.io/regan_data_img/2018/08/WX20180827-153226@2x.png)
![](https://regan_jeff.gitee.io/regan_data_img/2018/08/WX20180827-153239@2x.png)

#### 新功能
?>相比上个版本的Regan API新增了接口数据统计功能，包含模块数，接口数，参与人数的统计。以及时间热力图，周活跃度等图表的统计，精确的个人数据接口统计。

![](https://regan_jeff.gitee.io/regan_data_img/2018/08/WX20180827-172757@2x.png)
![](https://regan_jeff.gitee.io/regan_data_img/2018/08/WX20180827-172818@2x.png)
