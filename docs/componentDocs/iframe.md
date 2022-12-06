# iframe 嵌入网页

### 发展史
早起使用框架来创建网站 --- 网站的一小部分存储于单独的HTML页面中.

用每个框架来填充在屏幕上的区域。将网页分解成较小的块，这样有利于下载速度 —尤其是在那时网络连接速度太慢的情况下更为明显

### iframe 用途

iframe 提供了一种将整个web页嵌入到另一个网页的方法。适合将第三方内容嵌入您的网站.

可能无法直接控制，也不希望实现自己的版本 - 例如来自在线视频提供商的视频，Disqus等评论系统，在线地图提供商，广告横幅等.

### 属性
1. allowfullscreenL: 全屏
2. frameborder 边框
3. src
4. width / height
5. sandbox

### 优点：
1. iframe 能够原生不动的将嵌入的网页显示出来。
2. iframe 可以提供复用性，对一些公有的进行一个抽离，囊谦进去。
3. iframe 可以将一些第三方（不能自己开发的）内容和广告嵌入。
4. iframe 将页面进行划分，切成小的块，可以提供下载速度，在早期网络慢的情况下显著。

### 缺点：
1. iframe 会阻塞主页面的 onload事件（DOM加载完毕，资源也好了）,虽然不会阻塞DOM的解析。
2. 搜索引擎的检索不会解读这种页面，不利于 SEO.
3. iframe 和主页面共享连接， 页面超过 6 个 TCP 连接，就需要排队等候，会影响页面的并行加载。
4. iframe 嵌套进的网站，会出现各种滚动条。
5. 试图恶意修改您的网页或欺骗人们进行不想做的事情时常把iframe作为共同的攻击目标。
6. 单项劫持：黑客将隐藏的iframe嵌入到您的文档中， 来捕获用户的交互。


### 防止
1. 提供 sandbox 属性，给嵌入的内容仅能完成自己的工作权限。
2. 配置 CSP指令， CSP 代表安全的策略，提供一组HTTP头，提供HTM文档的安全性，这样子就防制其他网站嵌入。
3. 使用 HTTPS，HTTPS减少了远程内容在传输过程中被篡改的机会.