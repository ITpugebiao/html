# meta
用来描述文档的信息。

1. 比如 文档的字符集。 utf8

2. 文档的关键字、描述、作者。 

3. 以及HTTP标准固定的 name。 http-equiv="refresh"


4. viewport, 移动端适配。


5. 搜索引擎引用方式
```html
<meta name="robots" content="index,follow">
```
- all: 文件将被检索，链接也可以被查询。
- none: 都不可以。
- index: 文件被索引
- follow: 链接被查询。
- noindex: 文件将不被检索
- nofollow：页面上的链接不可以被查询。


6. 其他类型的元数据
Facebook 编写的元数据协议 Open Graph Data.  当你在 Facebook 上链接到你的链接，显示详细内容。
```html
<meta property="og:image" content="">
<meta property="og:description" content="">
<meta property="og:title" content="">
```

Twitter 协议
```html
<meta name="twitter:title" content="">
```
