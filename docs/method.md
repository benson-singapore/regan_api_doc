# Method注释配置


?> `Method` 注释信息样例：

``` java
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
```
!> 注：如果需要过滤controller中的方法，可在方法上添加 @ApiIgnore注解。

### text
  - 类型：String
  - 默认值：null
  - 可否为空：可为空
  - 样例：`用户登录功`
  - 说明：method注释文字 `方法功能说明`

### @title
  - 类型：String
  - 默认值：null
  - 可否为空：不能为空
  - 样例：`登录接口`
  - 说明：方法标题menu`子菜单标题`，method标题

### @param
  - 类型：String
  - 默认值：null
  - 可否为空：可为空
  - 样例：`@param username|用户名|string|必填`

?> method入参接口入参 <br>
  如：username|用户名|string|必填<br>
  <span style="color: #42b983; font-size: .8rem;font-weight: 500;">
  &nbsp;&nbsp;&nbsp;&nbsp;参数一：参数名<br>
  &nbsp;&nbsp;&nbsp;&nbsp;参数二：描述<br>
  &nbsp;&nbsp;&nbsp;&nbsp;参数三：参数类型<br>
  &nbsp;&nbsp;&nbsp;&nbsp;参数四：是否必填<br>
  </span>
  可接收多个参数。<br>
  注：如果入参为对象时可进行如下设置<br>
  <span style="color: #42b983; font-size: .8rem;font-weight: 500;">
  &nbsp;&nbsp;&nbsp;&nbsp;@param user|用户对象|object|必填<br>
  &nbsp;&nbsp;&nbsp;&nbsp;@param user.name|用户名|string|必填<br>
  &nbsp;&nbsp;&nbsp;&nbsp;@param user.password|密码|string|必填<br>
  </span>


### @resqParam
  - 类型：String
  - 默认值：null
  - 可否为空：可为空
  - 样例：`@resqParam username|用户名|string|必填`

?> method入参接口入参 <br>
  如：msg|消息信息|String|必填<br>
  <span style="color: #42b983; font-size: .8rem;font-weight: 500;">
  &nbsp;&nbsp;&nbsp;&nbsp;参数一：参数名<br>
  &nbsp;&nbsp;&nbsp;&nbsp;参数二：描述<br>
  &nbsp;&nbsp;&nbsp;&nbsp;参数三：参数类型<br>
  &nbsp;&nbsp;&nbsp;&nbsp;参数四：是否必填<br>
  </span>
  可接收多个参数。<br>
  注：如果入参为对象时可进行如下设置<br>
  <span style="color: #42b983; font-size: .8rem;font-weight: 500;">
  &nbsp;&nbsp;&nbsp;&nbsp;@resqParam user|用户对象|object|必填<br>
  &nbsp;&nbsp;&nbsp;&nbsp;@resqParam user.name|用户名|string|必填<br>
  &nbsp;&nbsp;&nbsp;&nbsp;@resqParam user.password|密码|string|必填<br>
  </span>

### @respBody
  - 类型：String
  - 默认值：null
  - 可否为空：可为空
  - 样例：
  `{
      "code":"000",
      "data":"",
      "msg":"success"
  }`
  - 说明：返回参数示例，`json字符串`

### @requestType
  - 类型：String
  - 默认值：null
  - 可否为空：可为空
  - 样例：`@requestType post`
  - 说明：数据请求类型，多个请求用逗号间隔`@requestType post,get`


### @author
  - 类型：String
  - 默认值：null
  - 可否为空：必填
  - 样例：`@author zhangby`

  ?> 指代controller `创建者`

  !> 接口数据的统计依据接口方法上的创建者为依据的，所以这里的创建者为必填，否则会不被统计


  ### @date
  - 类型：String
  - 默认值：null
  - 可否为空：可为空
  - 样例：`@date 2018/6/12 下午3:26`
  - 说明：创建时间
