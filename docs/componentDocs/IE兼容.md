# IE兼容
1. 如何实现 IE 下定义 1px 左右的宽度容器。
IE 默认的行高造成的，使用 overflow:hidden;zoom:0.08;line-height:1px

2. IE5-8不支持 opacity
```css
filter:alpha(opacity=60);  // IE5-7
-ms-filter: ""  // IE8
```

3. IE6 不支持 PNG 透明背景。
IE6下使用 gif 图片。

4. select 在 Ie6下遮盖
使用 iframe 嵌套。
