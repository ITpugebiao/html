# 矢量图标

### 两种图片方式
1. 位图使用像素网格来定义。
2. 矢量图使用算法来定义。


### 优点
1. 矢量图像看起来仍然效果很好且清晰, 无论它的尺寸如何，都使用算法来计算出图像的形状，仅仅是根据放大的倍数来调整算法中的值。
2. 矢量图中的文本仍然可以访问。 SEO 优化
3. SVG 可以很好地适应样式/脚本.


### 缺点：
1. SVG非常容易变得复杂, 在浏览器中可能会占用长的时间。
2. SVG可能比栅格图像更难创建.
3. 旧的版本不支持 SVG.


### 使用方法

#### 使用 img 标签

```html
<img
    src="equilateral.svg"
    alt="triangle with all three sides equal"
    height="87px"
    width="100px" />

```

```html
可以提高兼容性
<img src="equilateral.png" alt="triangle with equal sides" srcset="equilateral.svg">
```


### svg 标签
```html
<svg width="300" height="200">
    <rect width="100%" height="100%" fill="green" />
</svg>
```


### 使用 iframe 嵌入 SVG
```html
<iframe src="triangle.svg" width="500" height="500" sandbox>
    <img src="triangle.png" alt="Triangle with three unequal sides" />
</iframe>
```
缺点： 
1. iframe有一个回退机制，如果浏览器不支持iframe，则只会显示回退。
2. 除非 SVG 和您当前的网页具有相同的 origin.