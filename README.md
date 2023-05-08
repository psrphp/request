# library-request

请求数据便捷获取类

## 安装

``` cmd
composer require psrphp/request
```

## 用例

``` php
$request = new \PsrPHP\Request\Request('一个 \Psr\Http\Message\ServerRequestInterface 实例');

// 判断是否存在 支持server get post cookie file attr
$request->has('server.HTTP_HOST');
$request->has('get.name');
$request->has('post.title');
$request->has('cookie.id');
$request->has('file.cover');
$request->has('attr.login');

// 获取数据 支持server get post cookie file attr等方法
$request->get('somekey', 'defalut val..');
$request->server('HTTP_HOST', 'default val..');
$request->post('somekeyx', 'default val..');
$request->cookie('somekey', 'default val..');
$request->file('somekey', 'default val..');
$request->attr('someatt', 'default val..');
```
