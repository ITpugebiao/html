# link和@import区别

1. link是 XHTML 标签，除了可以加载 CSS, 还可以定义 RSS 等其他事物。 @import 是 CSS 范畴，只能够加载 CSS。
2. link 引入 CSS，在页面载入时并行加载。 @import需要等到网页完全载入后才能加载。
3. link 是 XHTML 标签，没有兼容性问题，@import是CSS2.1提出的。
4. link 支持使用 js 去控制 dom 改变样式。 @import 不支持。