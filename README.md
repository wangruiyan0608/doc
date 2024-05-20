# doc
这个是自动生成文档的工具
+ 采用解析注释生成文件的形式

## 安装
使用composer安装
~~~
composer require wangruiyan/doc
~~~


## 实例：
### 传入单个文件地址解析文档
~~~
use wangruiyan\Filed;

$filed = (new \Filed([
    'file_action_url'  => 'https://steam.yuanmadejia.com/'
]);

echo $filed->add_file(__DIR__."/Api.php")

// add_file 方法第二个参数可以不填写 是保存的文件路径
~~~

### 传入多个文件地址解析文档
~~~
use wangruiyan\Filed;

$filed = (new \Filed([
    'file_action_url'  => 'https://steam.yuanmadejia.com/'
]);

echo $filed->add_file([
    __DIR__."/Api.php",
    __DIR__."/Home.php",
]);
~~~

### 传入目录解析文档
~~~
use wangruiyan\Filed;

$filed = (new \Filed([
    'file_action_url'  => 'https://steam.yuanmadejia.com/'
]);

echo $filed->add_file(__DIR__);
~~~