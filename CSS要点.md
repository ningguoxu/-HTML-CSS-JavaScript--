# CSS要点

**什么是CSS？**
- 
 - CSS是一种样式表语言，它用来描述HTML或XML文档的呈现方式。CSS可以控制元素在屏幕、纸张、语音或其他媒体上的渲染效果。CSS的全称是Cascading Style Sheets，意思是层叠样式表，因为它可以让多个样式表按照一定的优先级规则来应用到同一个文档中。
 - CSS的基本语法是由选择器和声明组成的，选择器用来指定要应用样式的元素，声明用来定义元素的样式属性和值。例如，下面的代码表示将所有的\<h1>元素的颜色设置为蓝色，字体大小设置为36像素：
```
h1 {
  color: blue;
  font-size: 36px;
}
```

**选择器**
- 
 - 全局选择器:
    - 可以与任何元素匹配, 优先级最低, 一般做初始化样式
    - <b>代码示例:</b>
    ```
    * {
      margin: 0;
      padding: 0;
    }
    ```
  - 元素选择器:
    - HTML中\<b>, \<h1>到\<h6>, \<p>等
    - <b>代码示例: </b>
    ```
    p {
        color: red;
        font-size: 20px;
    }
    ```
  - 类选择器:
    - 用圆点"."来定义
    - <b>代码示例: </b>
    ```
    .oneclass {
        font-size: 30px;
        color: blue;
    }
    ```
  - 伪类选择器：
    - 伪类选择器是一种特殊的选择器，可以用来匹配元素的不同状态或位置
    - 常用选择器：
      - `:hover`，它可以用来设置鼠标悬停在元素上时的样式，比如改变颜色、背景、光标等。
      - `:focus`，它可以用来设置元素获得焦点时的样式，比如给输入框添加边框或阴影。
      - `:first-child`，它可以用来匹配作为父元素的第一个子元素的元素，比如给列表中的第一项添加特殊样式。
      - `:nth-child(n)`，它可以用来匹配作为父元素的第 n 个子元素的元素，比如给表格中的奇数行或偶数行添加不同的背景色。
      - `:not(selector)`，它可以用来排除匹配某个选择器的元素，比如选择所有不是段落的元素。


**字体属性**
- 
 - <b>color:规定文本的颜色</b>
    - 代码示例:
    -  ```
        div {color: red;}
        div {color: #ff0000;}
        div {color: rgb(255, 0, 0);}
        div {color: rgba(255, 0, 0, 1);}
        ```
  - <b>font-size设置文本大小</b>
    - ```
      h1 {font-size: 40px;}
      ```
    - <b>注意: </b>Chrome浏览器接受的最小字体是12px

  - <b>font-weight设置文本粗细</b>
    - 代码示例
    - ```
      p {font-weight: 900;}
      ```
    - <b>属性用法: </b>
    - | 值 | 描述 |
      | --- | --- |
      | bold | 定义粗体字符 |
      | bolder | 定义更粗的字符 |
      | lighter | 定义更细的字符 |
      | 100~900 | 定义由细到粗 400等同默认，而700等同于bold |
  - <b>font-style指定文本字体样式</b>
      |值|描述|
      |---|---|
      |normal|默认值|
      |italic|定义斜体字|
  - <b>font-family修改字体样式</b>
  ```
    p {
      font-family:Arial, Helvetica, sans-serif;
  }
  ```
**背景属性**
- 
 - <b>CSS背景属性主要有以下几个: </b>
 - |属性|描述|
   |---|---|
   |background-color|设置背景颜色|
   |background-image|设置背景图片|
   |background-position|设置背景图片显示位置|
   |background-repeat|设置背景图片如何填充|
   |background-size|设置背景图片大小|
 - <b>background-color属性: </b>
 ```
 .box1 {
   width: 600px;
   height: 400px;
   background-color: blue;
 }
 ```
 - <b>background-image属性: </b>
 ```
 .box2 {
     width: 400px;
     height: 400px;
     background-image: url(1.wepb);
 }
 ```
 - <b>background-repaet属性: </b>
   |值|说明|
   |---|---|
   |repeat|默认值|
   |repeat-x|只向水平方向平铺|
   |repeat-y|只向垂直方向平铺|
   |no-repeat|不平铺|

  - <b>background-size属性: </b>
    | 值 | 说明 |
    | :---: | :--- |
    | length | 设置背景图片的宽度和高度，第一个值宽度，第二个值高度，如果只是设置一个，第二个值auto |
    | percentage | 计算相对位置区域的百分比，第一个值宽度，第二个值高度，如果只是设置一个，第二个值auto |
    | cover | 保持图片纵横比并将图片缩放成完全覆盖背景区域的最小大小 |
    | contain | 保持图片纵横比并将图像缩放成适合背景定位区域的最大大小 |
  - <b>background-position属性: </b>
    | 值 | 说明 |
    | :---: | --- |
    | left top | 左上角 |
    | left center | 左中 |
    | left bottom | 左下 |
    | right top | 右上角 |
    | right center | 右中 |
    | right bottom | 右下 |
    | center top | 中上 |
    | center center | 中中 |
    | center bottom | 中下 |
    | x% y% | 第一个值是水平位置，第二个值是垂直位置，左上角是0％0％，右下角是100％100％。如果只指定了一个值，另一个值默认是50％。默认是0％0％ |
    | xpos ypos | 单位是像素 |
**文本属性**
- 
 - <b>text-align属性: </b>
    | 值 | 描述 |
    | :--- | :--- |
    | left | 文本居左排列，默认值 |
    | right | 把文本排列到右边 |
    | center | 把文本排列到中间 |

- <b>text-decoration属性: </b>
    | 值 | 描述 |
    | :---: | :---: |
    | underline | 定义下划线 |
    | overline | 定义上划线 |
    | line-through | 定义删除线 |

- <b>text-transform属性定义文本的大小写: </b> 
    | 值 | 描述 |
    | :---: | :---: |
    | capitalize | 定义每个单词开头大写 |
    | uppercase | 定义全部大写字母 |
    | lowercase | 定义全部小写字母 |
- <b>text-indent属性规定文本块中首行文本的缩进</b>
```
p {
    text-indent: 50px;
}
```
- <b>温馨提示: </b>负值是允许的, 如果是负值, 将第一行左缩进

**表格属性**
- 
 - 可以使用border属性, <b>border属性需要设置3个值, 分别是宽度, 样式, 颜色</b>

```
table, td {
    border: 1px solid blue;
}
```
 - 折叠边框
```
table, td {
    border: 1px solid blue;
}

/*折叠边框*/
table {
    border-collapse: collapse;
}
```
 - 可以用width和height规定表格的宽度, 高度
 - 表格的文字对齐(可以用text-align)
```
td {
    text-align: right;
}
```

```
td {
    height: 50px; vertical-align: bottom;
}
```
 - <b>表格填充: </b>可以用padding属性
 ```
 td {padding: 15px}
 ```
 - <b>表格颜色</b>
 ```
 table, td, th{border: 1px, solid green};
 td {background-color: green; color: red}
 ```

**关系选择器**
- 
  - <b>后代选择器</b>
    - <b>定义: </b>选择所有被 E 标签元素包含的 F 元素, 中间用空格隔开
      ```
      CSS:
      ul li {
          color: red;
      }

      HTML:
      <ul>
              <li>list1</li>
              <li>list2</li>
              <li>list3</li>
              <div>
                  <ol>
                      <li>list4</li>
                      <li>list5</li>
                      <li>list6</li>
                  </ol>
              </div>
          </ul>
      ```
    - <b>注意: </b>此时ol标签里的li标签也生效
  - <b>子代选择器</b>
    - 选择所有作为 E 标签的直接子元素 F , 对更深的一层不起作用, 用>表示
      ```
      E>F {}
      ```
  - <b>相邻兄弟选择器: </b>
    - 选择紧跟 E 元素的 F 元素, 用加号表示, 选择相邻的第一个兄弟元素, 只能向下选择
      ```
      HTML: 
      <h3>标题</h3>
      <p>段落1</p>
      <p>段落2</p>

      CSS:
      h3+p {
      color: blue;
      }
      ```
  - <b>通用兄弟选择器: </b>
    - 选择 E 标签之后的所有兄弟元素 F , 作用于多个元素, 用~隔开
      ```
      HTML:
          <h3>标题</h3>
          <p>段落1</p>
          <p>段落2</p>
          <b>文字1</b>
          <p>段落3</p>
      
      CSS:
        h3~p {
            color:#ff0000
        }
      ```

**布局方式**
- 
 - <b>流式布局：</b>流式布局是指元素按照文档流的顺序从上到下，从左到右依次排列，元素的宽度和高度可以根据内容或者百分比自适应。流式布局是最基本的布局方式，适用于简单的页面结构，也是移动端的常用布局方式。
 - <b>浮动布局：</b>浮动布局是指元素使用`float`属性脱离文档流，向左或者向右浮动，其他元素会围绕浮动元素排列。浮动布局可以实现多列布局，比如两栏布局、三栏布局等，也可以实现水平居中或者垂直居中。浮动布局需要注意清除浮动的问题，避免影响其他元素的布局。
 - <b>定位布局：</b>定位布局是指元素使用`position`属性脱离文档流，根据相对于父元素或者视口的位置进行定位。定位布局可以实现元素的精确控制，比如固定导航栏、弹出层等效果。定位布局需要注意元素的层叠顺序和定位参照物的问题。
 - <b>Flex布局：</b>Flex布局是指元素使用`display: flex`或者`display: inline-flex`属性，成为弹性容器，容器内的子元素成为弹性项目，可以按照一定的规则在水平或者垂直方向上排列和对齐。Flex布局可以实现多种复杂的页面效果，比如等高布局、圣杯布局、双飞翼布局等。Flex布局是一种现代的、灵活的、强大的布局方式，但是需要注意浏览器兼容性的问题。
 - <b>Grid布局：</b>Grid布局是指元素使用`display: grid`或者`display: inline-grid`属性，成为网格容器，容器内的子元素成为网格项目，可以按照定义好的网格线和网格区域进行排列和对齐。Grid布局可以实现更加精细和灵活的网格系统，比如瀑布流、日历、仪表盘等效果。Grid布局是一种最新的、最先进的、最强大的布局方式，但是也需要注意浏览器兼容性的问题。

**CSS盒子模型**
-  
 - padding（内边距）：是指内容周围的空间。可以给2个值, 一个是上下, 一个是左右
 - border（边框）：是紧接着内边距的线。需要给3个值, 分别是"大小, 样式, 颜色"
 - margin（外边距）：是围绕元素边界外侧的空间。是透明的
 - width：元素的宽度
 - background-color：元素内容和内边距底下的颜色
 - color：元素内容（通常是文本）的颜色
 - text-shadow：为元素内的文本设置阴影
 - display：设置元素的显示模式


 ```
body {
  width: 600px; /*强制页面永远保持 600 像素宽。*/
  margin: 0 auto; /*你在 margin 或 padding 这样的属性上设置两个值时，第一个值影响元素的上下方向（在这个例子中设置为 0）；第二个值影响左右方向。(这里，auto 是一个特殊的值，它将可用的水平空间平均分配给左和右）*/
  background-color: #ff9500; /*指定元素的背景颜色。我们给 body 用了一种略微偏红的橘色以与深蓝色的 <html> 元素形成反差，你也可以尝试其他颜色。*/
  padding: 0 20px 20px 20px; /*我们给内边距设置了四个值来让内容四周产生一点空间。这一次我们不设置上方的内边距，设置右边，下方，左边的内边距为 20 像素。值以上、右、下、左的顺序排列。与 margin 一样，你也可以像 Padding 语法中所记载的那样，使用一个、两个、三个或四个值。*/
  border: 5px solid black; /*这是为边框的宽度、样式和颜色设置的值。在本例中，它是一个在主体的所有侧面的 5 像素宽的纯黑色边框。*/
  }
  ```

**弹性盒子模型**
- 
 - 弹性盒子由弹性容器(Flex container)和弹性子元素(Flex item)组成
 - 通过设置'display'属性的值为'flex'
 - <b>温馨提示: </b>默认弹性盒里内容横向摆放
 - <b>flex-direction属性: </b>
    - flex-direction属性指定了弹性子元素在父容器中的位置
    - flex-direction: row|row-reverse|column|column-reverse
    - row: 横向从左到右排列(左对齐)
    - row-reverse: 反转横向排列(右对齐)
    - column: 纵向排列
    - column-reverse: 反转纵向排列
      ```
      flex-container {
          display: flex;
          flex-direction: column;
          width: 400px;
          height: 250px;
          background-color: lightgreen;
      }
      ```
  - <b>justify-content属性: </b>
    - 定义:内容对齐（justify—content）属性应用在弹性容器上，把弹性项沿着弹性容器的主轴线（main axis）对齐语法

    - 代码: ```justify-content:flex-start| flex-end | center ```
    - flex-start弹性项目向行头紧挨着填充。这个是默认值。第一个弹性项的main—start外边距边线被放置在该行的main—start边线，而后续弹性项依次平齐摆放
    - flex-end弹性项目向行尾紧挨着填充。第一个弹性项的main—end外边距边线被放置在该行的main—end边线，而后续弹性项依次平齐摆放
    - center弹性项目居中紧挨着填充。（如果剩余的自由空间是负的，则弹性项目将在两个方向上同时溢出）
    - <b>温馨提示: </b>水平属性用align-items(用法和上面相同)
  - <b>子元素上的属性: </b>
    - flex就是将子元素瓜分父容器的剩余空间
  
**文档流**
- 
 - <b>定义: </b>文档中可显示对象在排列时所占用的位置/空间

**浮动**
- 
 - float属性定义元素在哪个方向浮动, 任何元素都可以浮动
 - 原理: 浮动以后文档脱离了文档流, 浮动只有左右浮动, 没有上下浮动
   |用法|描述|
   |:---:|:---:|
   |left|元素向左浮动|
   |right|元素向右浮动|
```
box1 {
    float: left|right;
}
```
 - 当容器不足时, 会放在下一行
 - 当所有元素同时浮动时, 会变成水平摆放, 向左或者向右

**清除浮动**
- 
 - <b>浮动副作用: </b>
    - 浮动元素会造成父元素高度塌陷
    - 后续元素会受到影响
 - <b>清除浮动的方法: </b>
    - 父元素设置高度
        ```
        .container{
            height: 700px
        }
        ```
    - 受影响的元素增加clear属性
        ```
        .text{
            clear: left|both|right
        }
        ```
    - overflow清除浮动
      - 写在父级元素, 和clear: both一起用
    - 伪对象方式
      - 在父标签添加伪类`after`, 设置空的内容, 并且使用clear: both
        ```
        container::after {
            content: "";
            display: block;
            clear: both;
        }
        ```

**定位**
- 
 - `position`属性指定了元素的定位类型
    |值|描述|
    |:---:|:---:|
    |relative|相对定位|
    |absolute|绝对定位|
    |fixed|固定定位|
 - 其中, 绝对定位和固定定位会脱离文档流
 - <b>相对定位: </b>可以使用方向值`left, top, right, bottom`进行调整
 ```
 div {
    width: 200px;
    height: 200px;
    background-color: aqua;
    left: 200px;
    top: 100px;
 }
 ```
 - 设置定位之后，相对定位和绝对定位他是相对于具有定位的父级元素进行位置调整，如果父级元素不存在定位，则继续向上逐级寻找，直到顶层文档
 - `Z-index`属性设置元素堆叠顺序, 拥有更高堆叠顺序的元素会处于堆叠元素较低的前面.
 - 上下左右都居中
 ```
 div {
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    margin: auto;
 }
 ```
**CSS3新特性-圆角**
- 
  - `border-radius`属性可以给任意元素添加圆角, 使用规则如下:
      - 四个值：第一个值为左上角，第二个值为右上角，第三个值为右下角，第四个值为左下角
      - 三个值：第一个值为左上角，第二个值为右上角和左下角，第三个值为右下角
      - 两个值：第一个值为左上角与右下角，第二个值为右上角与左下角
      - 一个值：四个圆角值相同
      ```
      div {
          width: 50px;
          height: 50px;
          background-color: aqua;
          border-radius: 15px;
      }
      ```

**CSS3新特性-阴影**
- 
  - `box-shadow`向框添加一个或多个阴影
    ```
    div {box-shadow: h-shadow v-shadow blur color;}
    ```
    |值|描述|
    |:---|:---|
    |h-shadow|必选, 水平阴影的位置|
    |v-shadow|必选, 垂直阴影的位置|
    |blur|可选, 模糊距离|
    |color|可选, 阴影颜色|

**CSS3新特性-动画**
- 
 - 可以用百分比来规定变化发生的时间, 或用`from`和`to`(等同于0%和100%)
 - 使用`@keyframes`创建动画
 ```
 @keyframes name {
    0%{
        /* CSS样式 */
    }
    50%{
        /* CSS样式 */
    }
    100%{
        /* CSS样式 */
    }
}
 ```
 - 执行(播放)动画
    - `animation: name|duration|timing-function|delay|iteration-count|direction`
      | 值 | 描述 |
      |:---|:---|
      | name | 设置动画的名称 |
      | duration | 设置动画的持续时间 |
      | timing-function | 设置动画效果的速率（如下） |
      | delay | 设置动画的开始时间（延时执行） |
      | iteration-count | 设置动画循环的次数，infinite为无限次数的循环 |
      | direction | 设置动画播放的方向（如下） |
      | animation-play-state | 控制动画的播放状态：running代表播放，而paused代表停止播放 |

    - 设置动画速率
      | timing-function值 | 描述 |
      |:-------------------|:------|
      | ease              | 逐渐变慢（默认） |
      | linear            | 匀速 |
      | ease-in           | 加速 |
      | ease-out          | 减速 |
      | ease-in-out       | 先加速后减速 |

    - 设置动画播放的方向
      |direction值|描述|
      |:---:|:---|
      |normal|默认值为normal表示向前播放|
      |alternate|动画播放在第偶数次向前播放, 第奇数次向反方向播放|

**CSS3新特性-媒体查询**
- 
 - 媒体查询会根据设备的大小自动识别<b>加载不同样式</b>
 - 参数:
    - `width=device-width` : 宽度等于当前设备的宽度
    - `initial-scale` : 初始的缩放比例(默认设置1.0)
    - `maximum-scale` : 允许用户所放到最大比例(默认设置1.0)
    - `user-scalable` : 用户是否可以手动缩放(默认值为no)
  - <b>代码示例: </b>
```
HTML:
<div class="box"></div>

CSS:
  .box {
    width: 300px;
    height: 300px;
}

@media screen and (max-width:768px) {
    .box {
        background-color: darkturquoise;
    }
}

@media screen and (min-width:768px) and (max-width:996px) {
    .box {
        background-color: gainsboro;
    }
}

@media screen and (min-width:996px) {
    .box {
        background-color: red;
    }    
}
```

  - 注: 以上CSS代码中的设备尺寸分别是: 手机, 平板, 电脑
  - 如果想让元素在不同宽度下消失(或隐藏)只需加`display: none`, 想让他显示加`display: block`

**CSS Sprite-CSS精灵图**
- 
 - CSS Sprite也叫 CSS精灵图, CSS雪碧图, 它允许将网页中的零星图片整合到一张图片去
 - <b>优点: </b>减少图片字节, 减少HTTP请求, 从而大大提升网页性能
 - <b>原理: </b>