# H5拖拽API

拖拽：Drag。 释放：Drop。

源对象：指的是我们鼠标点击的一个事物，可以是任何事物。

目标对象：指的是我们拖放源对象后移动到一块区域，源对象可以进入这个区域。


### API
源对象触发的事件：
1. ondragstart 源对象开始被拖动。
2. ondrag: 源对象被拖动过程中。
3. ondragend: 源对象被拖动结束。


目标对象触发的事件：
1. ondragenter: 目标对象被源对象拖动着进入。
2. ondragover: 目标对象被源对象拖动着悬停在上方。
3. ondragleave：源对象拖动着离开目标对象。
4. ondrop：源对象拖动着在目标对象上方释放/松手。


### 在二者之间传递数据
e.dataTransfer {} // 数据传递对象。
用于在源对象和目标对象的事件间传递数据。

源对象保存数据。
e.dataTransfer.setData(k, v); // k, v string类型

目标对象上的事件处理中读取数据。
e.dataTransfer.getData(k); 


### 注意：
1. ondrag 事件最后一刻，无法读取鼠标的坐标， pageX 和 pageY 都是 0.
```javascript
if (x == 0 && y == 0) {
    return; // 不处理拖动最后一刻 X 和 Y 都是 0 的情况。
}
```

2. ondragover 有一个默认行为， 当 ondragover 触发时，ondrap 会失效。
(可能是浏览器的版本问题)。
```javascript
div.ondragover = function (e) {
    // 阻止默认行为，使得 drop 可以触发。
    e.preventDefault();
}

```

### 拖拽电脑文件上传

```javascript
电脑中拖拽一张图片到浏览器中实现的下载操作！！！ 
按照H5之前的标准，
要实现直接拖拽一张图片到浏览器中显示是无法完成！！但是自从H5新特性出来之后增加了拖拽API的特性，完美的实现了这一功能！！！

H5 新增的文件操作对象
File: 代表一个文件对象.
fileList: 代表一个文件列表对象，类数组。
FileReader: 用于从文件中读取数据。
FileWriter: 想文件中写出数据
e.dataTransfer.files[0] 找到拖放的文件
new FileReader() 创建文件读取器。
fs.radAsURLData 读取文件内容。
fr.onload = 读取完成
img.src = fr.result; 读取到的数据。


```