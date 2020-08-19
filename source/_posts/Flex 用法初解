# Flex 用法初解

### 前言


前端各端的迅速发展，促使了CSS样式的广泛使用，样式场景效果的创新也是种类繁多；其中布局对于需求的创新与实现起到了关键性的作用，不过往往有一些布局使用传统的方式得到的效果不尽人意；对此2009年，W3C提出了一种新的方案，即 [Flex](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout/Flexbox#%E4%B8%BA%E4%BB%80%E4%B9%88%E6%98%AF_%E5%BC%B9%E6%80%A7%E7%9B%92%E5%AD%90) 布局，它可以简便、迅速、完整、响应式的实现各种页面布局；继续往下阅读了解它与传统布局的差别吧。目前它已经得到了所有浏览器的支持，意味着现在能很安全的使用这项功能：![image.png](https://cdn.nlark.com/yuque/0/2020/png/315380/1589616855713-fcf0b636-a6df-4545-a10f-216b0a0165ed.png#align=left&display=inline&height=317&margin=%5Bobject%20Object%5D&name=image.png&originHeight=317&originWidth=899&size=114244&status=done&style=none&width=899)
相比于传统布局：
![image.png](https://cdn.nlark.com/yuque/0/2020/png/315380/1589615144728-d74a0672-2478-4f24-afe6-b78410d59ca6.png#align=left&display=inline&height=349&margin=%5Bobject%20Object%5D&name=image.png&originHeight=352&originWidth=403&size=104466&status=done&style=none&width=400)
传统布局的解决方式基于盒状模形，依赖于 [position](https://developer.mozilla.org/en-US/docs/Web/CSS/position) + [float](https://developer.mozilla.org/en-US/docs/Web/CSS/float) 属性；这些属性是唯一可靠且跨浏览器兼容的，不过该属性在特定的一些场景使用不尽人意。比如：

- 在父元素里面垂直居中一个块内容。
- 使容器的所有子项占用等量的可用宽度/高度，而不管有多少宽度/高度可用。
- 使多列布局中的所有列采用相同的高度，即使它们包含的内容量不同。



后续在学习使用 Flex 弹性盒子时，你会发现这类布局问题能简单并高效的解决




### 什么是Flex布局


- Flex 布局（全称：FlexiableBox，又名弹性盒子）
- 它定义了针对用户界面设计和一维项目布局而优化的CSS框模型，用来为盒状模型提供最大的灵活性。
- 在flex布局模型中，flex容器的子元素可以在任何方向上进行布局，并且可以“伸缩”它们的大小，既可以增长以填充未使用的空间，也可以收缩以防止父元素溢出。并且子元素的水平和垂直对齐都可以轻松操纵。





### 基本概念


采用 Flex 布局的元素，被称为 Flex 容器（flex container），简称：容器；它的所有子元素自动成为容器成员，称为 Flex 项目（flex item），简称：项目。如下图：
 ![image.png](https://cdn.nlark.com/yuque/0/2020/png/315380/1589622159730-d51e94de-f900-4178-82bd-7a994f4f0332.png#align=left&display=inline&height=333&margin=%5Bobject%20Object%5D&name=image.png&originHeight=333&originWidth=563&size=31056&status=done&style=none&width=563)
容器默认存在两条轴线：

- 水平的主轴（main axis）与垂直的交叉轴（cross axis）
- 主轴的开始位置（main start）与结束位置（main end）
- 交叉轴的开始位置（sross start）与结束位置（cross end）
- 项目默认沿主轴排列
   - 单个项目占据的主轴空间（main size）
   - 单个项目占据的交叉轴空间（sross size）





### 容器属性


- `flex-direction`
- `flex-wrap`
- `flex-flow`
- `justify-content`
- `align-items`
- `align-content`



容器有以上六个属性，下面来详解每个属性：


#### flex-direction

- 说明：该属性决定主轴的方向（即项目排列的方向）
- 用法：`.box { flex-direction: row | row-reverse | column | column-reverse; }`
- 属性值：
   - `row（默认）：主轴为水平方向，起点为左端`
   - `row-reverse：主轴为水平方向，起点为右端`
   - `column：主轴为垂直方向，起点为上沿`
   - `column-severse：主轴为垂直方向，起点为下沿`
- 效果（对应属性值）：

![flex-direction.png](https://cdn.nlark.com/yuque/0/2020/png/315380/1589774877409-7731bf74-4914-4cbb-b8ac-7a41e9ba3b20.png#align=left&display=inline&height=198&margin=%5Bobject%20Object%5D&name=flex-direction.png&originHeight=198&originWidth=743&size=14518&status=done&style=none&width=743)


#### flex-wrap

- 说明：项目默认情况下排在一条轴线；该属性定义如果一条轴线排不下时该如何换行
- 用法：`.box { flew-wrap: nowrap | wrap | wrap-severse; }`
- 属性值：
   - nowrap（默认）：不换行
   - wrap：换行，从上至下，第一行在上方
   - wrap-severse：换行，从下至上，第一行在下方
- 效果（对应属性值）：

![flex-wrap.png](https://cdn.nlark.com/yuque/0/2020/png/315380/1591669745727-84ae7aa7-87e0-43a6-ab1a-81a10f09beb0.png#align=left&display=inline&height=147&margin=%5Bobject%20Object%5D&name=flex-wrap.png&originHeight=147&originWidth=729&size=16032&status=done&style=none&width=729)


#### flex-flow

- 说明：该属性为`flex-direction`与`flex-wrap`属性的复合属性
- 用法：`.box { row nowrap; } 参考复合中的属性组合使用`
- 属性值：默认 row nowrap



#### justify-content

- 说明：该属性定义了项目在主轴上的对齐方式
- 用法：`.box { justify-content: flex-start | flex-end | center | space-between | space-around; }`
- 属性值：
   - flex-start（默认）：左对齐
   - flex-end：右对齐
   - center：居中
   - space-between：两端对齐，项目中间间隔相等
   - apace-around：每个项目两端相等（注意项目项目之间的间距比项目与边框之间的间距大一倍）
- 效果（对应属性值）：

![justify-content.png](https://cdn.nlark.com/yuque/0/2020/png/315380/1591670906245-d0047faf-e496-4099-9a7a-678f1088b505.png#align=left&display=inline&height=252&margin=%5Bobject%20Object%5D&name=justify-content.png&originHeight=252&originWidth=729&size=16930&status=done&style=none&width=729)


#### align-items

- 说明：该属性定义项目在交叉轴上的对齐方式
- 用法：`.box { align-items: stretch | flex-start | flex-end | center | baseline; }`
- 属性值：
   - stretch（默认）：项目未设置高度或者auto，将占满整个容器的高度
   - flex-start：交叉轴上沿对齐
   - flex-end：交叉轴下沿对齐
   - center：交叉轴居中对齐
   - baseline：项目的第一行文本基线对齐
- 效果（对应属性值）：

![align-items.png](https://cdn.nlark.com/yuque/0/2020/png/315380/1591673827328-00f3a848-dd3b-45a1-aede-ce58628d2b8f.png#align=left&display=inline&height=323&margin=%5Bobject%20Object%5D&name=align-items.png&originHeight=323&originWidth=745&size=19790&status=done&style=none&width=745)


#### align-content

- 说明：该属于定义了多条轴线的对齐方式（如果只有一条轴线，那么该属性不生效）
- 用法：`.box { align-content: stretch | flex-start | flex-end | center | space-between | space-stretch; }`
- 属性值：
   - stretch（默认）：轴线占满整个交叉轴
   - flex-start：与交叉轴的上沿对齐
   - flex-end：与交叉轴的下沿对齐
   - center：与交叉轴居中对齐
   - space-between：与交叉轴两端对齐，轴线与轴线中间间隔相等
   - space-stretch：每条轴线两侧的间距相等（注意轴线与轴线之间的间距比轴线与边框之间的间距大一倍）
- 效果（对应属性值）：

![align-content.png](https://cdn.nlark.com/yuque/0/2020/png/315380/1591675142916-6295ea7f-4b69-4f60-825d-faacf38a2a89.png#align=left&display=inline&height=378&margin=%5Bobject%20Object%5D&name=align-content.png&originHeight=378&originWidth=744&size=21451&status=done&style=none&width=744)


### 项目属性


- `order`
- `flex-grow`
- `flex-shrink`
- `flex-basis`
- `flex`
- `align-self`



项目有以上六个属性，下面来详解每个属性：


#### order

- 说明：该属性定义了项目的排序顺序；数值越小，排列越靠前，可负数，默认为0
- 用法：`.item { order: 0; }    /* default: 0 */`
- 效果：



#### flex-grow

- 说明：该属性定义了项目的放大比例；基于容器内所有项目根据数值进行比例放大，默认0
- 用法：`.item { flex-grow: 0; }    /* default: 0 */`
- 效果：



#### flex-shrink

- 说明：该属性定义了项目的缩小比例；基于容器内所有项目根据数值进行比例缩放，默认1
- 用法：`.item { flex-shrink: 1; }    /* default: 1 */`
- 效果：



#### flex-basis

- 说明：该属性定义了项目在分配多余空间之前，项目占据的主轴空间；浏览器根据该属性计算项目占据后的主轴的多余空间。占据的空间为项目的本来大小，默认auto
- 用法：`.item { flex-basis: auto | 数值（同width、height）; }    /* default: auto */`
- 效果：



#### flex

- 说明：该属性为`flex-grow`、`flex-shrink`、`flex-basis`三个属性的复合属性；默认0（建议优先使用该属性，而非单独写三个分离的属性，因为浏览器会推算相关值）
- 用法：`.item { flex: 0 | 1 | auto; }    /* default: 0 */`
- 效果：



#### align-self

- 说明：该属性允许单个项目不同于其他项目的对齐方式。可覆盖`align-items`属性，默认auto，表示继承父元素的`align-items`属性；如果没有父元素，则效果同于`stretch`属性
- 用法：`.item { align-items: auto | stretch | flex-start | flex-end | center | baseline;; }    /* default: auto */`
- 属性值：除`auto`外，其余属性均与`align-items`属性一致
- 效果：





### 注意事项


- 设置Flex布局后，子元素的`float`、`clear`、`vertical-align`属性都将失效
