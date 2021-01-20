# HTML入门笔记1



### HTML简介

HTML 是一种网页使用的语言，它定义了网页的结构和内容。其全名叫做“超文本标记语言”（HyperText Markup Language），由英国著名科学家李爵士（Tim Berners-Lee）于上世纪90年代初发明。

![李爵士](C:\Users\Administrator\Desktop\homework\Lee.jpg)      

​                        **李爵士**                       

### 一些必备的英语

|   英文    |    翻译    |    英文     |    翻译    |
| :-------: | :--------: | :---------: | :--------: |
|  heading  |    标题    |    order    | 顺序、秩序 |
|   body    | 身体、正文 |   ordered   |  有顺序的  |
| paragraph |    段落    |  unordered  |   无序的   |
|  section  |   章、节   | description |    描述    |
|  article  |    文章    |    term     |    术语    |
|   main    |    主要    |    data     |    数据    |
|   aside   |   旁边的   |    quota    |    引用    |
|  anchor   |  锚、定点  |    block    |     块     |
|  strong   |  重要、强  |   inline    | 内联、行内 |
| emphasis  |    强调    |    break    |    打断    |



### 辅助教材

一个用于教学及参考手册作用的网站：[网道](wangdoc.com)



### 插件的推荐

1. vscode中的：**prettier** 自动格式化 ctrl+\
2. 分享代码的**JSbin** ：

- 可以保存快照；
- 可以设置偏好；
- 可以使用ctrl+shift+L对齐代码；
3. 代码沙盒：**codesanbox.io**

   

### html起手式

即html文件建立时的标准模板，如下介绍：

`<!DOCTYPE html>`   

**文档类型**

`<html lang="en">`   

**html标签，lang表示语言类型，可以将其改为zh-cn**

`<head>` 

**表示头部位置（通常写一些看不见的东西）**

       ` <meta charset="UTF-8">`  

​        **文件的字符编码**

        `<meta name="viewport" content="width=device-width, initial-scale=1.0">`

​         **禁用缩放，兼容手机**

​        `<meta http-equiv="X-UA-Compatible" content="ie=edge">`

​         **告诉IE使用最新内核**

​         <font face="黑体" color=green>注意：这段代码有可能你的VScode是没有的，可以使用[自定义模板](https://www.jianshu.com/p/fe027008dacf)进行设置</font>

​         `     <title>Document</title>`

​         **标题**


   ``` 

</head>

<body>

</body>

</html>
   ```

### html章节标签

其意义在于像书或文章一样表示其层级

- 标题 h1~h6
- 章节 section
- 文章 article
- 段落 p
- 头部 header <font face="黑体" color="green">通常用于广告</font>
- 脚部 footer  <font face="黑体" color="green">通常用来注释版权所有等信息</font>
- 主要内容 main
- 旁支内容 aside
- 划分 div

### 全局属性

本属性即可以在所有html标签都可以使用的属性，如:
                                                               `<div class="middle">`

- class     <font face="黑体" color="green">用来对网页元素进行分类。如果不同元素的`class`属性值相同，就表示它们是一类的</font>
- contenteditable    <font face="黑体" color="green">使任何一个元素变得可以直接编辑,如可以让style元素进入body区，直接进行调试</font>
- hidden   <font face="黑体" color="green">隐藏任何一个元素，可通过css调出</font>
- id   <font face="黑体" color="green">在网页内的唯一标识符,万不得已不要用，用class</font>
- style  <font face="黑体" color="green">用来指定当前元素的 CSS 样式,style效力对比：js>html>css</font>
- tabindex   <font face="黑体" color="green">制定tab键跳动焦点及是否可以遍历，正数表示顺序访问，0表示最后访问，-1表示不访问</font>
- title   <font face="黑体" color="green">用来为元素添加附加说明</font>

### 默认样式

- **什么事默认样式？**
   <font face="黑体" color="800080" size="3">在css未出世前，html本身就有的一些样式，如标题自动加粗等</font> 
- **如何查看默认样式？**
   <font face="黑体" color="800080" size="3">首先打开Chrome</font>
   <font face="黑体" color="800080" size="3">Elements->Styles->user agent stylesheet</font>
- **User Agent是什么？**
   <font face="黑体" color="800080" size="3">即浏览器的意思</font>
- **为何使用CSS reset？**
   <font face="黑体" color="800080" size="3">由于html本身的默认样式已经不符合我们的需求，所以使用css reset将其覆盖掉，使用我们喜欢的样式</font>

### 常见的CSS reset

- 个人使用的[CSS reset](C:\Users\Administrator\Desktop\note\html\reset.css)

- 还可以在大厂等网页进行抄写

  <font face="黑体" color="800080" size="3">随意找个body元素，找到h1、h2、h3、h4等元素，点击index，找到相关元素后三击该行+复制</font>

### 内容标签

html中一些表示内容或对内容产生作用的标签：

- ol+li（ordered list + list item）

  <font face="黑体" color="green">按照顺序的列表+列表某一项</font>

- ul+li (undrdered list + list item)

  <font face="黑体" color="green">不按照顺序的列表+列表某一项</font>

- dl + dt +dd (description list + term + data)

  <font face="黑体" color="green">描述列表+描述项目+描述资料</font>

- pre (preview 缩写)

  <font face="黑体" color="green">会保留所有的空格或回车</font>

  <font face="黑体" color="green">html多个连续的空格或回车会被合成一个空格或回车</font>

- hr  

  <font face="黑体" color="green">分割线的意思(无需闭合)</font>

- br (break 的缩写) 

  <font face="黑体" color="green">换行的意思（无需闭合）</font>

- a (anchor 缩写) 

  <font face="黑体" color="green">超链接，属性加：targe="_blank"可在新窗口打开</font>

- em (emphasis 的缩写)  

  <font face="黑体" color="green">强调的意思，句子中的强调，语气强调</font>

- strong

  <font face="黑体" color="green">同样为强调，页面中的强调，强调内容本身</font>

- code

  <font face="黑体" color="green">多数用于包裹代码</font>

- q （quote 的缩写）

  <font face="黑体" color="green">引用的意思，其在页面中无效果</font>

- blockquote

  <font face="黑体" color="green">换行引用</font>

### [练习副本](http://js.jirengu.com/peqes/12/edit?html,output)

