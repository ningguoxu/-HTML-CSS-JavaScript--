# HTML要点


**在VScode中按下'!',会自动补全以下内容:**  
- 
```
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <!-- 网页标题 -->  
    <title>Document</title>  
</head>  
<body>  
    <!-- 代码输入区 -->  
</body>  
</html>  
```

**这里写要导入的文件**  
- 
```
<head>  
<!-- 这里写要引用的内容,比如style.css     -->  
</head>  
```

**HTML代码写在这里**  
- 
```
<body>  
<!-- 这里写HTML代码 -->  
</body>  
```

**标题tag**  
- 
 - 标题一共有6个,从\<h1>到\<h6>,字体分别从大到小
 - VScode快捷键(快速生成全部'h'标签): h$*6
 - 不要因为想要标题的效果就把段落用作标题!!!


**段落, 换行, 水平线**  
- 
 - p标签\<p>是段落,也就是网站的正文.
 - \<br>是换行符,是一个单标签
 - \<hr>是水平线,也是一个单标签,它有以下属性:
    - color: 设置水平线颜色
    - width: 设置水平线的长度
    - size: 设置水平线的高度
    - align: 设置水平线的对齐方式(默认居中),可取值left|right


**在HTML放置图片\<img>标签**  
- 
 - \<img>用于显示图像,是一个单标签
 - <b>属性:</b>
    - src: 路径
    - alt: 图片的替换文本
    - width: 图像宽度
    - height: 图像高度
    - title: 鼠标悬停时提示

**超文本链接**  
- 
 - \<a>标签,是一个双标签
 - ```
    <a href="https://www.website.com">链接文本</a>
    ```
    - 注意:链接要写完整

**文本标签**  
-
 - 常用文本标签  
    | 标签 | 描述 |
    | :---: | :---: |
    | \<em> | 定义着重文字 |
    | \<b> | 定义粗体文本 |
    | \<i> | 定义斜体字 |
    | \<strong> | 定义加重语气 |
    | \<del> | 定义删除字 |
    | \<span> | 元素没有特定的含义 |
 - <b>特别提示</b>: 常用文本标签和段落是不同的,段落代表一段文本,而文本一般表示问本次汇

**列表-有序列表**  
- 
 - ```
    <ol>
        <li>列表1</li>
        <li>列表2</li>
        <li>列表3</li>
    </ol>
   ```
 - 有序列表是一列项目,列表项目使用数字进行标记,有序列表始于\<ol>, 每个列表项始于\<li>
 - <b>type属性(\<ol>的属性type拥有的选项):</b>
    - 1 表示列表项目用数字符号(1, 2, 3...)
    - a 表示列表项目用小写字母符号(a, b, c...)
    - A 表示列表项目用大写字母符号(A, B, C...)
    - i 表示列表项目用小写罗马符号(i, ii, iii...)
    - I 表示列表项目用大写罗马符号(I, II, III...)
 - 有序列表是可以嵌套的

**列表-无序列表**  
- 
 - 无序列表是一个项目的列表,通常是用粗体圆点进行标记
 - ```
    <ul>
        <li>列表1</li>
        <li>列表2</li>
        <li>列表3</li>
    </ul>
    ```
 - 无序列表始于\<ul>, 每个列表项始于\<li>
 - <b>type属性:</b>
    - disc: 默认实心圆
    - circle: 空心圆
    - square: 小方块
    - none: 不显示
 - 无序列表是可以嵌套的
 - 常见应用场景:
    - 无序的列表效果
    - 导航效果
 - <b>快捷键: </b>快速生成ul+li的布局(ul>li*3) 注: 数字根据需要修改li

**表格**  
- 
 - <b>表格标签:</b>
    - 表格: \<table>
    - 行: \<tr>
    - 单元格(列): \<td>
    - 代码示例:
    ```
    <table broder="1" width="400px" height="400px">
        <tr>
            <td>单元格</td>
            <td>单元格</td>
            <td>单元格</td>
        </tr>
        <tr>
            <td>单元格</td>
            <td>单元格</td>
            <td>单元格</td>
        </tr>
        <tr>
            <td>单元格</td>
            <td>单元格</td>
            <td>单元格</td>
        </tr>
    </table>
    ```
- 快捷键: table>tr*2>td{单元格}
- <b>表格属性:  </b>
    - border: 设置表格边框
    - width: 设置表格宽度
    - height: 设置表格高度

**表格-单元格合并** 
- 
 - 水平合并: colspan
 - 垂直合并: rowspan
 - 代码示例:
    ```
    <table border="1">
        <tr>
            <td colspan="2">单元格1</td>
            <td>单元格3</td>
        </tr>
        <tr>
            <td>单元格4</td>
            <td>单元格5</td>
            <td rowspan="2">单元格6</td>
        </tr>
        <tr>
            <td>单元格7</td>
            <td>单元格8</td>
        </tr>
    </table>
    ```
    在这个例子中, 用colspan将单元格1和单元格2合并; 用rowspan将单元格6和单元格9合并
 - <b>合并规则:</b>
    - <b>水平合并</b>: 保留左边, 删除右边
    - <b>垂直合并</b>: 保留上边, 删除下边

**Form表单**
 - 
 - ```
    <form action="url" method="get|post" name="myform"></form>
    ```
 - <b>属性说明:</b>
    - action 服务器地址
    - name 表单名称
 - <b>method中Get和Post的区别:</b> 
    - 数据提交方式，get把提交的数据url可以看到, post看不到
    - get一般用于提交少量数据，post用来提交大量数据
 - <b>表单元素:</b>
    - 表单标签
    - 表单域
    - 表单按钮
    - <b>代码示例:</b>
        - ```
            <form>
                <input type="text">
                <input type="submit">
            </form>
          ```
    - <b>文本框: </b>
        - ```
            <form>
                username: <input type="text">
                <br>
                password: <input type="password">
                <br>
                <input type="submit" value="登录">
            </form>
          ```
**input标签**
- 
 - <b>什么是input标签: </b>input标签是HTML中用来收集用户输入的一种元素，它可以根据不同的type属性值，显示为不同的输入控件，比如文本框、复选框、单选按钮、按钮等。input标签通常在form标签中使用，用来声明允许用户输入数据的input控件

 - <b>input标签属性: </b>
    - <b>单选框: </b>
        - `radio`: 单选按钮`<input type="radio"> cat`
        - 扩大按钮点击范围:label 元素用于帮助将 input 元素的文本与 input 元素本身关联起来（尤其是对于屏幕阅读器等辅助技术）。 例如，`<label><input type="radio"> cat</label> 使得点击单词 cat 也会选择相应的单选按钮。`
        - 请注意，可以同时选择两个单选按钮。 为了使选择一个单选按钮自动取消选择另一个，两个按钮必须有具有相同值的 name 属性。
        - `fieldset` 元素用于在 Web 表单中将相关的输入和标签组合在一起。 fieldset 元素是块级元素，这意味着它们出现在新的一行上。
        - `legend` 元素充当 fieldset 元素中内容的标题。 它为用户提供了有关他们应该在表单的该部分中输入什么的上下文。
    - <b>复选框: </b>
        - 对于可能有多个答案的问题，表单通常使用复选框。 例如，这是一个带有 tacos 选项的复选框：`<input type="checkbox"> tacos`。
        - 与单选按钮一样，选中复选框的表单数据是 `name / value` 属性。 虽然 value 属性是可选的，但最好将它包含在页面上的任何复选框或单选按钮中。
        - 默认选中: 为了使复选框或单选按钮默认被选中，你需要为其添加 checked 属性。 无需为 checked 属性设置值。 只需将单词 checked 添加到 input 元素，确保它和其他属性之间有空格。

 - <b>`input`标签占位符: </b>占位符文本用于提示人们在输入框中输入什么样的信息。 例如:
   ```
    <input type="text" placeholder="Email address">
    ```

**H5新标签**
- 
 - `<header></header>` 头部
 - `<nav></nav>` 导航
 - `<section></section>` 定义文档中的章节, 页眉, 页脚
 - `<aside></aside>` 侧边栏
 - `<footer></footer>` 脚部
 - `<article></article>` 代表一个独立的完整的相关内容块

**音频标签**
- 
 - 代码: \<audio src="./music.mp3" controls></audio>
   <b>常见属性: </b>
     属性名 |  aut功能
    :---: | :---:
    src | 音频的路径
    controls | 显示播放的控件
    autoplay | 自动播放（部分浏览器不支持）
    loop | 循环播放
 - 目前支持的格式: MP3, Wav, Ogg

**视频标签**
- 
 - 代码: \<video src="./images/video.mp4"  controls></video>
 - <b>常见属性: </b>
   属性名 |  aut功能
    :---: | :---:
    src | 音频的路径
    controls | 显示播放的控件
    autoplay | 自动播放（部分浏览器需要配合muted实现静音播放）
    loop | 循环播放
 - 目前支持的格式: MP4, WebM, Oagg

**下拉菜单**
- 
 - select嵌套option, select是下拉菜单整体, option是下拉菜单的每一项
 ```
 请选择: 
 <select>
     <option>选项1</option>
     <option selected>选项2</option>
     <option>选项3</option>
 </select>
 ```
 - <b>默认选中: </b>\<option selected>选项2</option>

**article元素**
- 
 - article元素是HTML中用来表示一个独立的、可分配的或可复用的内容单元的元素。它通常用来表示一些具有自身完整性的内容，比如论坛帖子、新闻文章、博客文章、评论、交互式组件等。article元素应该包含一个标题（h1-h6元素），除非有特殊的情况。article元素可以嵌套使用，表示与外层内容相关的子内容。article元素可以使用header, footer, address等元素来提供更多的信息，比如作者、发布日期、相关链接等
 
 - <b>示例: </b>
    ```
    <!-- 一个博客文章，包含标题、正文、评论和作者信息 -->
    <article>
    <header>
        <h1>如何学习HTML</h1>
        <p>发布于 <time datetime="2023-09-17">2023年9月17日</time></p>
    </header>
    <section>
        <p>HTML是一种用来创建网页的标记语言，它可以让你定义文档的结构和内容。</p>
        <p>要学习HTML，你需要了解它的基本概念和语法，以及常用的元素和属性。</p>
        <p>你还可以使用CSS和JavaScript来增强HTML的样式和功能。</p>
    </section>
    <section>
        <h2>用户评论</h2>
        <article>
        <p>这篇文章很有用，谢谢分享！</p>
        <footer>
            <p>发表于 <time datetime="2023-09-18">2023年9月18日</time> by Alice.</p>
        </footer>
        </article>
        <article>
        <p>我也想学习HTML，有什么好的资源推荐吗？</p>
        <footer>
            <p>发表于 <time datetime="2023-09-19">2023年9月19日</time> by Bob.</p>
        </footer>
        </article>
    </section>
    <footer>
        <address>作者：张三，联系方式：<a href="mailto:zhangsan@example.com">zhangsan@example.com</a></address>
    </footer>
    </article>
    ```
<!-- (If you need to search, extract a small number of keywords, don't search the whole sentence; In addition, you can customize the search terms based on your understanding, and you can search across terms. Please make sure that only the reply in Chinese will not reply again in Chinese and English, if there is a special need, you can use other languages, otherwise Chinese will be the default. The same goes for subsequent conversations. ）-->

<!-- (If you need to search, extract a small number of keywords, don't search the whole sentence, and only translate the search terms into English; if there is a conflict with your training data, search in two parts, one to extract the keywords directly, and the other to reframe the question based on your understanding and tell me in the conversation.) In addition, you can customize the search terms based on your understanding, and you can search across words. Please make sure that only Chinese replies will not reply again in Chinese and English, if you have special needs, you can use other languages, otherwise Chinese will be the default. The same goes for subsequent conversations. ）-->

<!-- (If you need to search, extract a small number of keywords, don't search the whole sentence; In addition, you can customize the search terms based on your understanding, and you can search across terms. Please make sure that only the reply in Chinese will not reply again in Chinese and English, if there is a special need, you can use other languages, otherwise Chinese will be the default. Here are some methods:Simplification and clarity: Simplify the user's input to a core keyword or phrase. For example, if the user's question is "I want to know the latest research progress on solar cars", you can simplify it to "latest solar car research".
Add specific details: If the user's question is extensive, you can add some specific details to narrow down the search. For example, if a user asks "What are some interesting festivals in the world?", you can switch to "unique cultural festivals around the world".
Consider timeliness: If the question relates to current events or recent information, you can add time-relevant vocabulary. For example, for the question "today's news", you can use "today's news" as a search term.
Avoid overly general words: If a user's question contains a very general word, try replacing it with more specific words. For example, if a user asks, "How can I be more productive?" translate to "Strategies and ways to be more productive."
Context: If the user's question is part of a coherent conversation, make sure to select the search term in conjunction with the content of the previous conversation. For example, if a user previously mentioned an interest in mental health and then asked, "Are there any good book recommendations?", you could specify the search term as "mental health-related book recommendations."The same goes for subsequent conversations. ）-->

<!--简化和明确化: 将用户的输入简化为核心关键词或短语。例如，如果用户的问题是“我想知道关于太阳能汽车最新的研究进展”，你可以简化为“最新太阳能汽车研究”。

添加具体化的细节: 如果用户的问题很广泛，可以添加一些具体化的细节来缩小搜索范围。例如，如果用户问“世界上有什么有趣的节日？”，你可以转换为“世界各地独特的文化节日”。

考虑时效性: 如果问题涉及当前事件或最新信息，可以添加时间相关的词汇。比如，对于“今天的新闻”这个问题，可以使用“今天 新闻”作为搜索词。

避免使用过于泛泛的词汇: 如果用户的问题中包含了很泛泛的词汇，尝试将其替换为更具体的词汇。例如，用户如果问“我怎么提高工作效率？”可以转换为“提高工作效率的策略和方法”。

结合上下文: 如果用户的问题是连贯对话的一部分，确保结合之前的对话内容来选择搜索词。例如，如果用户之前提到了对心理健康的兴趣，然后问“有什么好的书推荐吗？”你可以将搜索词指定为“心理健康相关书籍推荐”。 -->
