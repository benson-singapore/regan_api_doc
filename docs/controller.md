# Controller注释配置


?> `Controller` 注释信息样例：

``` java
/**
 * 用户管理
 * @action /user
 * @author zhangby
 * @date 2018/6/12 下午3:26
 */
public class UserController extends Controller{

}
```

### text
  - 类型：String
  - 默认值：null
  - 可否为空：不能为空
  - 样例：`用户管理`

?> controller注释文字`menu主菜单名`

### @action
  - 类型：String
  - 默认值：null
  - 可否为空：不能为空
  - 样例：`@action /user`

?> 对应的Controller`路由配置`
```java
//jfinal对应的Controller路由配置
/** * 配置路由 */
@Override
public void configRoute(Routes me) {
  //配置api路由
  me.add("/user", UserController.class);
}
//即：@action /user


//springboot 配置指的是 @RequestMapping 配置的路由
/**
 * 用户管理
 * @action /user
 * @author zhangby
 * @date 2018/8/24 下午5:55
 */
@Controller
@RequestMapping("/user")
public class UserController {
}
//即：@action /user

```

### @author
  - 类型：String
  - 默认值：null
  - 可否为空：可为空
  - 样例：`@author zhangby`

?> 指代controller `创建者`


!> 接口统计中，这里的创建者不会作为接口数据的统计。接口数据的统计是依据接口方法上的创建者为依据的


### @date
- 类型：String
- 默认值：null
- 可否为空：可为空
- 样例：`@date 2018/6/12 下午3:26`
- 说明：创建时间
