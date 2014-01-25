QQ Connect SDK for Ruby On Rails
================

### 警告:
此版本是fork别人的，主要解决了对ruby1.8.7的兼容问题

从`0.1.1`开始,重新设计了整套SDK,因此并不向下兼容.

若你不需要使用新的API,则可以保留旧版本.

### 安装:
    
在你的Gemfile里新增一行

`gem 'qq', :git => 'git://github.com/046569/qq.git'`

然后

`bundle install`

### 使用:

在你喜欢的地方定义:

`APPID='你的ID'`

`APPKEY='你的key'`

`REDURL='&redirect_uri=你的跳转地址'`

回调页示例(获取用户昵称)：

```Ruby
user=Qq.new(params[:code],request.env['HTTP_CONNECTION'])
user.get_user_info('https://graph.qq.com/user/get_user_info')['nickname']
```

相关参数请查阅[QQ互联开放平台](http://connect.qq.com/intro/login/)


### 授权:

MIT
