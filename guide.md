# 指南

#### 1.安装
  - Regan API 基于jfinal/springboot框架构建。

    ?> 可参考：[jfinal](http://www.jfinal.com/) | [springboot](https://spring.io/projects/spring-boot)

  - maven依赖
    ``` xml
<dependency>
  <groupId>cn.hutool</groupId>
  <artifactId>hutool-all</artifactId>
  <version>4.0.12</version>
</dependency>
<dependency>
  <groupId>com.google.guava</groupId>
  <artifactId>guava</artifactId>
  <version>18.0</version>
</dependency>
<dependency>
  <groupId>com.alibaba</groupId>
  <artifactId>fastjson</artifactId>
  <version>1.2.9</version>
</dependency>
    ```

- 加入 src下api包下的文件，以及 api目录里的html相关的页面

- jfinal 需要 配置api路由

   ``` java
/**
 * 配置路由
 */
@Override
public void configRoute(Routes me) {
    //配置api路由
    me.add("/api", ApiController.class);
}
   ```

#### 2.配置文件说明
  - jfinal
  在项目resources 加入 api.properties 文件，指定解析的包文件。
  ``` properties
  #解析的controller包 多个用逗号间隔
  packages=com.jfinal.api.controller

  #需要过滤的controller 多个用逗号间隔
  filters=UserController

  #主题色，黑：dark、白：light
  theme=dark
  ```
  - springboot

  ``` yaml
  # api配置信息
  api:
      #解析的controller包
      packages:
        - com.regan.api.jboot.controller
      #需要过滤的controller
      filters:
      #主题色，黑：dark、白：light
      theme: dark
  ```

#### 3.服务启动注意：

- 按照jfinal / springboot 项目配置正常访问就可以。

 ?> 默认访问地址为：http://localhost:端口/api

 !> 由于Regan API，是基于注释开发的。在开发环境中可正常访问，因为Regan API是直接访问源码数据读取注释等信息的。
 但是项目线上部署时编译后的java文件是没有注释的，所以访问不到这也是为了安全考虑。
