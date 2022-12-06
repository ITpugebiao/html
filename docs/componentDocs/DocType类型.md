# DocType类型
### DocType写与不写
DocType 不写浏览器会使用自己的怪异模式解析渲染页面. 

DocType 被提供，将会以标准模式解析渲染。


### DocType 的几种模式
DocType 必须放到每一个文档的顶部，在所有代码和标识之上。

DocType 不是 HTML 标签，指示 web 浏览器关于页面使用哪个 HTML 版本进行编写的的指令；在 HTML 4.01 中，声明要引入 DTD。 HTML 4.01 是基于 SGML 的。DTD 规定了标记语言的规则, 这样浏览器才能正确的呈现内容。HTML5 不是基于 SGML 的，所以不需要引入 DTD。


### HTML 4.01 Strict
DTD 包含了所有 HTML 元素和属性，但是不包括展示性和弃用的元素（font）。不允许框架集（Framesets）.

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">


### HTML 4.01 Transitional
该 DTD 包含所有 HTML 元素和属性, 包括展示性的和弃用的元素（比如 font）。不允许框架集（Framesets）.

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" 
"http://www.w3.org/TR/html4/loose.dtd">

### HTML 4.01 Frameset
该 DTD 等同于 HTML 4.01 Transitional，但允许框架集内容。

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" 
"http://www.w3.org/TR/html4/frameset.dtd">




### DTD
DTD的作用在于定义SGML文档的文档类型以便于浏览器解析.


### HTML5
HTML5 标准放弃了与 SGML 的兼容，不需要引入 DTD. 保留 DOCTYPE 是为了保证与旧浏览器的兼容. 选用 <!DOCTYPE html> 是因为这个声明格式在当前所有的浏览器 下都会以标准模式渲染并且长度最短。

