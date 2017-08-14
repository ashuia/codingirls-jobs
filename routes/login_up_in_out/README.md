## 注册登录登出
### 注册模块
1. 需要信息 用户名 + 邮箱 + 密码 + 确认密码
2. 过程
用户注册填写信息 --> 前端基本验证信息 -->  (将基本信息保存到数据库,此时为未激活状态)   -->  给用户发送邮件  -->  用户点击邮件(访问固定激活API，更改用户信息状态，为激活状态。可以实现登录)

### 登录模块
1. 需要信息  用户名（邮箱） + 密码
2. 过程
用户输入登录信息   --> 验证用户是否注册 --(success)-->  验证用户账户是否为激活状态  -->  是：提示登录成功(否：提示需要发送邮件进行激活)  --> 登陆成功，保持用户session，进入首页

### 登出模块
1. 需要信息  用户session
2. 过程
用户点击注销(登出按钮) --> 调用注销API -->删除在服务器中的session -->注销成功，跳转首页   
