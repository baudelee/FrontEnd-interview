[前端需要注意哪些SEO](#前端需要注意哪些seo)

[web开发中会话跟踪的方法有哪些](#web开发中会话跟踪的方法有哪些)

[Doctype作用? 严格模式与混杂模式-如何触发这两种模式](#doctype作用)

[行内元素有哪些？块级元素有哪些？](#行内块级元素有哪些)

[CSS的盒模型](#CSS的盒模型)

[link和import的区别是什么](#link和import的区别是什么)

[CSS选择符属性继承优先级算法以及CSS3新增伪类新特性](#css选择符属性继承优先级算法以及css3新增伪类新特性)

[img的title和alt有什么区别](#img的title和alt有什么区别)





### 前端需要注意哪些SEO

1. 合理的title、description、keywords：搜索对着三项的权重逐个减小，title值强调重点即可，重要关键词出现不要超过2次，而且要靠前，不同页面title要有所不同；description把页面内容高度概括，长度合适，不可过分堆砌关键词，不同页面description有所不同；keywords列举出重要关键词即可
2. 语义化的HTML代码，符合W3C规范：语义化代码让搜索引擎容易理解网页
3. 重要内容HTML代码放在最前：搜索引擎抓取HTML顺序是从上到下，有的搜索引擎对抓取长度有限制，保证重要内容一定会被抓取
4. 重要内容不要用js输出：爬虫不会执行js获取内容
5. 少用iframe：搜索引擎不会抓取iframe中的内容
6. 非装饰性图片必须加alt
7. 提高网站速度：网站速度是搜索引擎排序的一个重要指标



### web开发中会话跟踪的方法有哪些

1. cookie
2. session
3. url重写
4. 隐藏input
5. ip地址

### doctype作用

1. <!DOCTYPE> 声明位于文档中的最前面，处于 <html> 标签之前。告知浏览器的解析器，

​        用什么文档类型 规范来解析这个文档。 

2. 严格模式的排版和 JS 运作模式是  以该浏览器支持的最高标准运行。


3. 在混杂模式中，页面以宽松的向后兼容的方式显示。模拟老式浏览器的行为以防止站点无法工作。
4. DOCTYPE不存在或格式不正确会导致文档以混杂模式呈现。



### 行内块级元素有哪些

1.CSS规范规定，每个元素都有display属性，确定该元素的类型，每个元素都有默认的display值，

​    比如div默认display属性值为“block”，成为“块级”元素；

​    span默认display属性值为“inline”，是“行内”元素。  

2.行内元素有：a b span img input select strong（强调的语气） 

​     块级元素有：div ul ol li dl dt dd h1 h2 h3 h4…p  



### CSS的盒模型

box-sizing   两种 content-box 标准盒模型   border-box  IE 盒模型

标准盒模型： 内容(content)、填充(padding)、边界(margin)、 边框(border)

IE 的content   部分包含了 border 和 pading;



### link和import的区别是什么

1.link属于XHTML标签，而@import完全是CSS提供的一种方式;

2.页面被加载的时候，link-会同时被加载，而@import引用的CSS会等到页面被加载完再加载;

3.import只有在IE5以上的才能识别，而link是XHTML标签，无兼容问题;

4.link方式的样式的权重 高于@import的权重.



### css选择符属性继承优先级算法以及css3新增伪类新特性



##### CSS 选择符：

1. id选择器(# myid)


2. 类选择器(.myclassname)
3. 标签选择器(div, h1, p)
4. 相邻选择器(h1 + p)
5. 子选择器(ul > li)
6. 后代选择器(li a)
7. 通配符选择器( * )
8. 属性选择器(a[rel = "external"])
9. 伪类选择器(a: hover, li:nth-child)

##### 可继承的样式：

1. font-size
2. font-family
3. color
4. text-indent

##### 不可继承的样式：

1. border
2. padding
3. margin
4. width
5. height

##### 优先级算法：

1. 优先级就近原则，同权重情况下样式定义最近者为准;
2. 载入样式以最后载入的定位为准;
3. !important >  id > class > tag  
4. important 比 内联优先级高，但内联比 id 要高

##### CSS3新增伪类举例：

1. p:first-of-type  选择属于其父元素的首个 p 元素的每个 p 元素。
2. p:last-of-type   选择属于其父元素的最后 p 元素的每个 p元素。
3. p:only-of-type  选择属于其父元素唯一的 p元素的每个 p 元素。
4. p:only-child     选择属于其父元素的唯一子元素的每个p 元素。
5. p:nth-child(2)  选择属于其父元素的第二个子元素的每个p 元素。
6. :enabled :disabled 控制表单控件的禁用状态。
7. :checked         单选框或复选框被选中。

##### CSS3有哪些新特性？

1. CSS3实现圆角（border-radius），阴影（box-shadow），
2. 对文字加特效（text-shadow、），线性渐变（gradient），旋转（transform）
3. transform:rotate(9deg) scale(0.85,0.90) translate(0px,-30px) skew(-9deg,0deg);// 旋转,缩放,定位,倾斜
4. 增加了更多的CSS选择器  多背景 rgba 
5. 在CSS3中唯一引入的伪元素是 ::selection.
6. 媒体查询，多栏布局
7. border-image



### img的title和alt有什么区别

1. title是[global attributes](http://www.w3.org/TR/html-markup/global-attributes.html#common.attrs.core)之一，用于为元素提供附加的advisory information(咨询信息)。通常当鼠标滑动到元素上的时候显示。
2. alt是<img>的特有属性，是图片内容的等价描述，用于图片无法加载时显示、读屏器阅读图片。可提图片高可访问性，除了纯装饰图片外都必须设置有意义的值，搜索引擎会重点分析。

