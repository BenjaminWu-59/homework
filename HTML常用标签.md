# HTML重难点标签

### 一些难点单词

---

|   英语    | 翻译 |  英语  |   翻译   |
| :-------: | :--: | :----: | :------: |
|   hyper   | 超级 | blank  |   空白   |
|  target   | 目标 | parent | 父母之一 |
| reference | 引用 |  self  |   自己   |
|   frame   | 边框 |  load  |   加载   |
|   error   | 错误 | canvas |   画布   |



### a标签

---

通常链接通过`<a>`标签表示，在用户点击后，浏览器会跳转到指定的网址

- **属性**

  **href** （hyper reference 即超链接）

  例：`<a href="http://google.com">超链接</a>`

  **target** （指定如何展示打开的链接）

  例：`<a href="http://google.com" target="_blank"> 超链接</a>`   新页面打开链接

  **download**（下载该网页,具体看[网道](https://wangdoc.com/html/link.html)）

  例：`<a href="demo.txt" download>下载</a>`

  **rel=noopener**

- **作用**

​       跳转外部网页

​       跳转内部锚点

​       跳转到邮箱or电话等

**注意：**不要双击html打开网页！！！ (大概率导致路径错误)

​            **可以使用**:  终端-> hs . -c-1 -> ctrl+单击任意网址 -> 网址后面加入文件名（推荐）

​            **也可以使用**：终端 -> parcel 文件名（如：a-href.html）-a-href.html -> ctrl+单机网址



### a href 的取值

---

- **网址**

  `https://google.com `

  加密的传输协议

  `http://google.com `

  未加密的传输协议

  `//google.com `

  使用此方式可自动识别协议（比较高级）

  ***使用方式***： 

  ​        使用hs或parcel打开html文件  **->**  在页面中打开开发者工具  **->**  点击network **->**  勾选  Preserve log  **->** 点击超链接  **->**  文件跳转后即可在Name **-->** Headers中查看跳转过程![](https://github.com/BenjaminWu-59/homework/blob/main/picture/1.png)

  

- **路径**

  **/a/b/c** 以及 **a/b/c**

  **index.html** 以及 **./index.html** （两者的意思都是在当前目录寻找index.html文件）

- **伪协议**

   **javascript:代码;**

   *例*：

  1. ` <a href="javascript:alert(1);">JS伪协议</a>`  即执行该代码

  2. `<a href="javascript:;">查看</a>`  即使得`<a>`标签什么也不做

     假设代码为<a href="">查看</a>,则你可以看到点击该链接，页面将刷新。因此要使得`<a>`标签什么也不做，必须用 **javascript:;**空代码。

   **mailto:邮箱**

   跳转到指定的邮箱

   **tel:手机号**

   跳转到指定的手机号（直接打电话）

- **id**

​         **href=#xxx** 跳转到指定的标签位置（自己试验一下）

​         `  <a href="href=#xxx">标签</a>`



### a的 target 取值

---

- **内置名字**

  **_self**（当前页面打开，是默认的值）

  **_blank**（新的页面打开链接）

  **_top**（最上级的页面打开）

  **_parent**（上一级页面打开）

  ***worning***： *_top 和 _parent 的用法具体来说，我们可以建立一个新的多层级的页面。*

  ​                  **top用法**：*假设这个页面共有3层页面，那么使用无论第2层还是第三层使用top       时，都会由第一层页面打开。*

  ​                  **parent用法**：*假设这个页面共有3层页面，那么第2层使用时，会由第一层打开，第三层使用时，会由第二层打开。*

  

- **程序员命名**

  **window 的 name**
```
   <a href="//baidu.com" target="xxx">BaiDu</a>
   <a href="//google.com" target="xxx">google</a>
```
​        如以上代码，点击百度后，再点击google时，百度会被google覆盖，“xxx”的意思是target指向的目标被绑定为xxx。

​        可以在被打开的网页的开发者工具中打开console -> 输入：window.name，得到的结果为：“xxx”

​       **inframe 的 name**
```
   <a href="//baidu.com" target="xxx">BaiDu</a>
   <a href="//google.com" target="yyy">google</a>
   <hr/>
   <iframe src="" name="xxx"></iframe>
   <iframe src="" name="yyy"></iframe>
```

​       以上代码会在同一个页面中显示两个小窗口，这两个小窗口随着你点击链接会变成相应网站。“xxx” 和 “yyy” 具有定位作用。



### a 的 download

---

作用在于下载页面，而非打开页面。并不是所有浏览器都支持，尤其是手机浏览器。



### table（表格）标签

---

- **相关标签**

  **table**  表格标签（插入表格）

  **thead** 表格头部 （可以没有）

  **tbody** 表格身体（必须有的标签）

  **tfoot** 表格尾部 （可以没有）

  **tr** table里面的一行，即table row

  **th** 表头，表格第一行或第一列，加粗效果

  **td** 表格数据 table data

  

- **相关样式**

​       **table-layout**  定义了用于布局表格*单元格*，*行*和*列*的算法 

​                 `table-layout: auto;`
​                大多数浏览器采用自动表格布局算法对表格布局。**表格及单元格的宽度取决于其包含的内容**(个性化定制)

​                 `table-layout: fixed;`
​                表格和列的宽度通过表格的宽度来设置，**某一列的宽度仅由该列首行的单元格决定**（平均分配）

​       **border_collapse**

​                使表格合并，去除分框模式

​       **boeder_spacing**      

​               相邻单元格边框之间的距离（只适用于分框模式）



### img标签

---

- **作用**

  发出get请求，从而展示一张图片

- **属性**

    **alt** 对图像的文本描述（非强制性）

    **height** 图片高

    **width** 图片宽

    注意：同时使用宽和高时，图片会变形！！ 只使用其中一个，它会按照比例裁定。

    **src**  source的缩写，即链接图片所在位置

- **事件**

  **onload**和**onerror**

  可以测定图片加载成功或失败的原因，并在开发者工具中显示（console）

  列：

  ```
  <img id="xxx" src="sea.png" alt="" />
  
      <script>
  
        xxx.onload = function () {
  
          console.log("图片加载成功");
  
        };
  
        xxx.onerror = function () {
  
          console.log("图片加载失败");
  
        };
  
      </script>
  
  ```

  以上代码，在img中加入id=“xxx”，下面JS代码中可引入此id，查询图片加载状况：

  ​                        开发者工具 -> console -> 刷新页面 -> 跳出图片加载成功或失败 

  

- **响应式**

     即，使图片可以在手机等其他设备上正常阅览：
```
    img {
          max-width: 100%;
          }
```
      加上这句话即可

- **可替换元素**

​        即CSS 可以影响可替换元素的位置，但不会影响到可替换元素自身的内容。img是其中之一。

​        其他看[可替换元素类型](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Replaced_element)

### form标签

---

- **作用**

  发送get或post请求，然后刷新页面

- **属性**

  **action** 即指定发送的url

  **metod** 即指定发送的方法

  **autocomplete** 自动完善，会有一些建议在表单自动出现

  如：

  ![](C:\Users\Administrator\Desktop\note\html\piture\2.png)
  **target** 怎么打开页面，以a标签的target基本相同

  代码形式：
```
  <form action="/yyy" method="post" autocomplete="on">

        <input name="username" type="text" />

        <input type="submit" value="提交" />

  </form>
```
- **事件**

     onsubmit

     由于input内部不能再设置其他元素，因此使用button来设置可以更自由的修改按钮内容
```

      <form action="/yyy" method="post" autocomplete="on">

      <input name="username" type="text" />

      <input type="submit" value="电风扇继续提交" />

      <button type="submit">

        <strong>继续搞</strong>

      </button>

    </form>

```

​    **注**：type="submit"是input和button共用一个按钮内容的前提



### input标签

---

- **作用**

  可以让用户输入内容

- **属性**

    **类型type**：button (按钮) / checkbox(多选) /  email / file（选择上传的文件）/ hidden（用于js等自动填写ID等东西） / number / password / radio(单选) / search / submit（发送请求） / tel / text（简单的框空行）

    **其他**：name / autofocus / checked / disabled / pattern / value 等

- **事件**

  onchange / onfocus / onblur

- **验证器**

  一些html5的新增功能，自行了解



### 其他输入标签

---

- **标签**

  **select+option** 创建一个多选的单个框文本
```
<select>
      <option value="">- 请选择 -</option>
      <option value="1">星期一</option>
      <option value="2">星期二</option>
</select>
```
​       以上代码实际效果为：

![](C:\Users\Administrator\Desktop\note\html\piture\3.png)



  **textarea ** 一个多行纯文本编辑控件
```
  <textarea style="resize: none; width: 50%; height: 100px"></textarea>
```
​      以上代码创建了一个多行文本控件，由resize控制其属性



​      **label**



- **注意事项**

​       一般不监听 input 的 click 事件

​      form里面 input 必须有 name

​      form里面放一个 type=submit 才能触发 submit 事件



### 感想

---

这些东西要硬记就太难了，只能说多做一些项目，抓大放小的去熟练了！
