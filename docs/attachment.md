# 附件

#### api页面功能定制

?> 如果需要对页面功能进行修改和单独定制的话，可在gitee上下载源码进行自由定制。地址：[https://gitee.com/regan_jeff/Regan_API_Source](https://gitee.com/regan_jeff/Regan_API_Source)

该项目是基于`react`开发的，前端ui基于阿里`飞冰`。项目启动部署与编译如果对node不熟悉可借助飞冰[ICEWorks](https://alibaba.github.io/ice/iceworks)工具,如果对node熟悉的话可借助命令去编译启动项目。

#### 本地启动
 - 依赖node环境，可自行安装
 - gitee上下载[Regan_API_Source](https://gitee.com/regan_org/Regan_API_Source)项目源码
 - 初始化，进入项目根目录初始化项目。 `npm init`
 - 项目启动，`npm start`
 - 项目构建，`npm build`

!> <span style="color:#f66">注：</span><br>
  1.&nbsp;&nbsp;由于本地启动需要依赖接口，所以需要下载[Regan_API](https://github.com/zhangbiy/regan_api)源码，并在本地启动服务保证接口可正常访问。<br>
  2.&nbsp;&nbsp;修改跨域配置，修改根目录文件 `.webpackrc.js`，指定API接口地址。<br>
  3.&nbsp;&nbsp;项目部署，更改完相应的配置后，执行项目构建。把生成的 js css html三个文件，放入[Regan_API](https://github.com/zhangbiy/regan_api)项目中，正常访问即可。

#### Regan_API_Source 插件介绍

  - 页面UI，[飞冰](https://alibaba.github.io/ice)
  - 图表，[echarts](https://www.npmjs.com/package/echarts)，[echarts-for-react](https://www.npmjs.com/package/echarts-for-react)
  - 剪贴板，[react-copy-to-clipboard](https://www.npmjs.com/package/react-copy-to-clipboard)
  - json数据展示，[react-json-view](https://www.npmjs.com/package/react-json-view)
