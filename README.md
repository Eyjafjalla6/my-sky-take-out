# my-sky-take-out

经典苍穹外卖项目
* **项目描述**：管理端可以对商品的分类、订单、员工等信息进行管理维护，统计各类数据；用户可以通过微信小程序端浏览菜单、下单支付，并跟踪订单状态。餐厅端则可以接收订单、管理库存，并安排配送。

* **使用技术**：Spring、SpringMVC、SpringBoot、MySQL、Mybatis、Redis、Jwt、WebSocket、Nginx、Vue

1. 使用Nginx作为http服务器，部署静态资源，实现反向代理和负载均衡。
2. 通过WebSocket向前端传输数据，实现来单提醒功能，以及利用SpringTask定时任务实现订单的超时处理，超时自动取消订单；
3. 通过redis来缓存菜品数据，减少数据库查询操作。
4. 调用百度地图API检测收货地址是否超过配送范围。使用阿里云oss存储菜品图像文件。为防止接口被恶意调用，设计API秘钥、令牌校验等方式来提高接口安全性。
5. 使用AOP编程实现公共字段自动填充。


微信支付没有运营执照只能魔改注释掉。

