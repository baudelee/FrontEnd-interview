[前端需要注意哪些SEO](#前端需要注意哪些seo)

[web开发中会话跟踪的方法有哪些](#web开发中会话跟踪的方法有哪些)

[Doctype作用? 严格模式与混杂模式-如何触发这两种模式](#doctype作用)

[行内元素有哪些？块级元素有哪些？](#行内块级元素有哪些)

[CSS的盒模型](#CSS的盒模型)

[link和import的区别是什么](#link和import的区别是什么)

[CSS选择符属性继承优先级算法以及CSS3新增伪类新特性](#css选择符属性继承优先级算法以及css3新增伪类新特性)

[img的title和alt有什么区别](#img的title和alt有什么区别)

[HTML全局属性(global attribute)有哪些](#html全局属性有哪些)

[什么是web语义化,有什么好处](#什么是web语义化和有什么好处)

[HTTP method](#httpmethod有哪些)





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



### html全局属性有哪些

- accesskey:设置快捷键，提供快速访问元素如[aaa](https://github.com/qiu-deqing/FE-interview#)在windows下的firefox中按alt + shift + a可激活元素
- class:为元素设置类标识，多个类名用空格分开，CSS和javascript可通过class属性获取元素
- contenteditable: 指定元素内容是否可编辑
- contextmenu: 自定义鼠标右键弹出菜单内容
- data-*: 为元素增加自定义属性
- dir: 设置元素文本方向
- draggable: 设置元素是否可拖拽
- dropzone: 设置元素拖放类型： copy, move, link
- hidden: 表示一个元素是否与文档。样式上会导致元素不显示，但是不能用这个属性实现样式效果
- id: 元素id，文档内唯一
- lang: 元素内容的的语言
- spellcheck: 是否启动拼写和语法检查
- style: 行内css样式
- tabindex: 设置元素可以获得焦点，通过tab可以导航
- title: 元素相关的建议信息
- translate: 元素和子孙节点内容是否需要本地化



### 什么是web语义化和有什么好处



web语义化是指通过HTML标记表示页面包含的信息，包含了HTML标签的语义化和css命名的语义化。 

HTML标签的语义化是指：通过使用包含语义的标签（如h1-h6）恰当地表示文档结构 

css命名的语义化是指：为html标签添加有意义的class，id补充未表达的语义

为什么需要语义化：

- 去掉样式后页面呈现清晰的结构
- 盲人使用读屏器更好地阅读
- 搜索引擎更好地理解页面，有利于收录
- 便团队项目的可持续运作及维护



### httpmethod有哪些

1. 一台服务器要与HTTP1.1兼容，只要为资源实现**GET**和**HEAD**方法即可
2. **GET**是最常用的方法，通常用于**请求服务器发送某个资源**。
3. **HEAD**与GET类似，但**服务器在响应中值返回首部，不返回实体的主体部分**
4. **PUT**让服务器用请求的主体部分来创建一个由所请求的URL命名的新文档，或者，如果那个URL已经存在的话，就用干这个主体替代它
5. **POST**起初是用来向服务器输入数据的。实际上，通常会用它来支持HTML的表单。表单中填好的数据通常会被送给服务器，然后由服务器将其发送到要去的地方。
6. **TRACE**会在目的服务器端发起一个环回诊断，最后一站的服务器会弹回一个TRACE响应并在响应主体中携带它收到的原始请求报文。TRACE方法主要用于诊断，用于验证请求是否如愿穿过了请求/响应链。
7. **OPTIONS**方法请求web服务器告知其支持的各种功能。可以查询服务器支持哪些方法或者对某些特殊资源支持哪些方法。
8. **DELETE**请求服务器删除请求URL指定的资源




### CSS单位有哪些

#### rem em

我们将从你已经熟悉的东西开始。`em`单位被定义为当前字体大小。例如，如果你在`body`元素上设置一个字体大小，那么在`body`元素内的任何子元素的`em`值都等于这个字体大小。

```javascript
<body>
<div class="test">Test</div>
</body>
body { font-size: 14px; }
div { font-size: 1.2em; // calculated at 14px * 1.2, or 16.8px }
```

在这里，我们说这个`div`将有一个`1.2em`的`font-size`。它是所继承的字体大小的`1.2`倍，在这个例子中为`14px`。结果为`16.8px`.

当你在每个元素内都级联`em`定义的字体大小将会发生什么？在下面的代码片段中我们应用和上面一模一样的CSS.每个`div`从它们的父节点继承字体大小，带给我们逐渐增加的字体大小。

```javascript
<body>
<div>
Test <!-- 14 * 1.2 = 16.8px -->
<div>
Test <!-- 16.8 * 1.2 = 20.16px -->
<div>
Test <!-- 20.16 * 1.2 = 24.192px -->
</div>
</div>
</div>
</body>
```

虽然在某些情况下可能需要这个，但是通常你可能想基于一个唯一的度量标准来按比例缩放。在这种情况下，你应该用`rem`。`rem`中的”`r`“代表”`root`“；这等同于`font-size`基于根元素进行设置；在大多数情况下根元素为`html`元素。



```css
html { font-size: 14px; }
div { font-size: 1.2rem; }
```

`rem`不是只对定义字体大小有用。比如，你可以使用`rem`把整个网格系统或者UI样式库基于HTML根元素的字体大小上,然后在特定的地方使用`em`比例缩放

```css
container {
	width: 70rem; // 70 * 14px = 980px
}
```



#### vh和vw (ie11 以上都兼容)

响应式网页设计技术很大程度上依赖于比例规则。然而，CSS比例不总是每个问题的最佳解决方案。CSS宽度是相对于最近的包含父元素。如果你想使用显示窗口的宽度或高度而不是父元素的宽度将会怎么样？这正是`vh`和`vw`单位所提供的。

`vh`等于viewport高度的`1/100`.例如，如果浏览器的高是`900px`,`1vh`求得的值为`9px`。同理，如果显示窗口宽度为`750px`,`1vw`求得的值为`7.5px`。

这些规则表面上看起来有无尽的用途。例如，做一个占满高度的或者接近占满高度的幻灯片，可以用一个非常简单的方法实现，只要用一行CSS：



```css
.slide {
	height: 100vh;
}
```

#### vmin 和 vmax（ie11不兼容）

`vh`和`vm`总是与视口的高度和宽度有关，与之不同的，`vmin`和`vmax`是与这次宽度和高度的最大值或最小值有关，取决于哪个更大和更小。例如，如果浏览器设置为`1100px`宽、`700px`高，`1vmin`会是`7px`,`1vmax`为`11px`。然而，如果宽度设置为`800px`，高度设置为`1080px`，`1vmin`将会等于`8px`而`1vmax`将会是`10.8px`。

所以你什么时候可能用到这些值？

设想你需要一个总是在屏幕上可见的元素。使用高度和宽度设置为低于`100`的`vmin`值将可以实现这个效果。例如，一个正方形的元素总是至少接触屏幕的两条边可能是这样定义的：

```css
box {
height: 100vmin; width: 100vmin;
}
```

[![img](https://lucius0.github.io/images/css/css-24.png)](https://lucius0.github.io/images/css/css-24.png)

如果你需要一个总是覆盖可视窗口的正方形(一直接触屏幕的四条边),使用相同的规则只是把单位换成`vmax`。

```css
.box {
height: 100vmax; width: 100vmax;
}
```

[![img](https://lucius0.github.io/images/css/css-25.png)]()

这些规则的组合提供了一个非常灵活的方式，用新的、令人兴奋的方式利用你的可视窗口的大小。



#### ex和ch （ex 几乎都不支持  ch ie 11 部分不支持，edge 完全支持）

`ex`和`ch`单位，与`em`和`rem`相似，依赖于当前字体和字体大小。然而，与`em`和`rem`不同的是，这两个单位只也依赖于`font-family`，因为它们被定为基于特殊字体的法案。



