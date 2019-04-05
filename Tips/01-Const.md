在项目中通常会定义很多的常量，可以在常量类中使用接口来区分不同组的常量：

```java
/**使用内部接口来把常量进行分组*/
public class Const {
    /**
     * 用户组
     */
    public interface Role{
        /**普通用户*/
        int ROLE_CUSTOMER = 0;
        /**管理员*/
        int ROLE_ADMIN = 1;
    }
    /**
     * 购物车组
     */
    public interface Cart{
        /**购物车选中状态*/
        int CHECKED = 1;
        /**购物车未选中状态*/
        int UN_CHECKED = 0;

        /**库存数量限制失败，用于返回给前端*/
        String LIMIT_NUM_FAIL = "LIMIT_NUM_FAIL";
        /**库存数量限制成功，用于返回给前端*/
        String LIMIT_NUM_SUCCESS = "LIMIT_NUM_SUCCESS";
    }
}
```

