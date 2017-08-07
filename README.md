# SimpleHtml
一款PHP语言开发的HTML DOM解析插件，语法类似于Jquery，基于[simplehtmldom](http://simplehtmldom.sourceforge.net/)做了命名空间的封装。
## 安装
```
    composer require jiangxianli/simple-html
```
## 使用
```php
//1.抓取网站源码
$url = 'https://baidu.com';
$html = file_get_content($url);
//2.初始化解析器
$html_node = SimpleHtml\SimpleHtml::str_get_html($html);
//使用选择器
$title = $html_node->find('title',0)->innertext;
print_r($title);
//清除使用
$html_node->clear();
```

## 更多语法
请查看[simplehtmldom](http://simplehtmldom.sourceforge.net/)