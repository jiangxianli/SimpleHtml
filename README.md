# SimpleHtml
一款PHP语言开发的HTML DOM解析插件，语法类似于Jquery，基于[simplehtmldom](http://simplehtmldom.sourceforge.net/)做了命名空间的封装。
## 安装
```
    composer require jiangxianli/simple-html
```
## 使用
```php
//字符串加载
$html = \SimpleHtml\SimpleHtml::str_get_html(''<html><body>从字符串中加载html文档演示</body></html>'');
//URL加载
$html = \SimpleHtml\SimpleHtml::str_get_html('https://baidu.com');
//文件加载
$html = \SimpleHtml\SimpleHtml::str_get_html('/tmp/baidu.html');

//查找html文档中的超链接元素
$a = $html->find('a');

//查找文档中第(N)个超链接，如果没有找到则返回空数组.
$a = $html->find('a', 0);

// 查找id为main的div元素
$main = $html->find('div[id=main]',0);

// 查找所有包含有id属性的div元素
$divs = $html->find('div[id]');

// 查找所有包含有id属性的元素
$divs = $html->find('[id]');

//清除使用
$html->clear();
```

## 更多使用语法
- [simPHP Simple HTML DOM Parser Wiki](http://simplehtmldom.sourceforge.net/manual.htm)
- [PHP Simple HTML DOM解析器使用入门](http://www.cnphp.info/php-simple-html-dom-parser-intro.html)