<a name="uNzE9"></a>
## HTML
- 网页分为header和body，分别表示网页头部以及网页身体部分，主要我们写代码就是在body写。
<a name="wFlLT"></a>
## 基本标签
标题标签 就是 h1 ～ h6，段落标签 p 水平线hr 换行br 粗体和斜体分别是strong 和 em

<a name="zSRSx"></a>
## 图像标签
img 基本形态为：
```html
<img src="https://cdn.learnku.com/uploads/images/201912/29/1/U2rJPAUCt5.jpeg!large" alt="gopher" title="悬停文字" width="" height=""> 
```
分别为源路径，图片加载失败时显示的文字，鼠标放上图片显示的文字以及宽度和高度

<a name="fvU0D"></a>
## 链接标签

1. 链接标签主要是a
```html
<a herf="https://baidu.com" target="_self">点击我试试<a/>
```
a标签有一个herf代表来源，target分为不同的打开模式，**_self表示在本标签页打开，_blank表示新建一个标签页打开**。

2. 锚链接 需要一个锚标记，点击这个就可以跳转到标记的地方
3. 功能性链接比如可以放mail和javascript
```html
<a href="mailto:1072830776@qq.com">点击联系我</a>
<a href="javascript:alert('哈哈哈哈')">你好</a>
```

<a name="spbZT"></a>
## 列表标签

1. 有序列表
```html
<ol>
  <li>Java</li>
  <li>Python</li>
  <li>Go</li>
  <li>C</li>
  <li>侧开</li>
</ol>
```

2. 无序列表
```html
<ul>
    <li>Java</li>
    <li>Python</li>
    <li>Go</li>
    <li>C</li>
    <li>测开</li>
</ul>
```

3. 自定义列表
```html
<dl>
    <dt>标签</dt>
    <dd>Java</dd>
    <dd>python</dd>
    <dd>go</dd>
    <dd>cpp</dd>
</dl>
```
<a name="L7aly"></a>
## 表格标签
table 和 tr 和 td，table表示表格，tr表示行，td表示列，然后在td里面有一个熟悉叫做rowspan和colspan分别是跨行和跨列
```html
<table  border="1px">
  <tr >
    <!--跨列 colspan-->
    <td colspan="4">1-1</td>
  </tr>
  <tr>
    <td rowspan="2">2-1</td>
    <td>2-2</td>
    <td>2-3</td>
    <td>2-4</td>
  </tr>
  <tr>
    <td>3-1</td>
    <td>3-2</td>
    <td>3-3</td>
  </tr>
</table>
```
<a name="DHJGp"></a>
## 音视频标签
```html
<!--媒体元素包含音频和视频-->
<!--video 和 audio-->
<!--controls 代表控制台 autoplay代表自动播放-->
<video src="../resource/video/消毒.mp4" controls autoplay>消毒的视频</video>
<audio src="../resource/audio/青城山下%20-%20KKECHO,REDBOI.mp3" controls autoplay></audio>
```
<a name="qounJ"></a>
## 页面结构
分为header网页头部，footer网页底部，以及nav是导航类

<a name="bQoc3"></a>
## 内联框架标签
iframe内联框架 就是把其他的网页放到我们自己的网页中
```html
<!--内联框架 就是把其他的网页放到我们自己的网页中 -->
<iframe src="https://bing.com" frameborder="0" height="800px" width="1000px" name="a"></iframe>
```
<a name="ZkMg9"></a>
## 表单（重要）
表单主要就是form，其中包括action：表单提交的地方可以是网站也可以是一个请求处理地址，method就是提交方法一般是get或者post
```html
<form action="1.%20theFirstWeb.html" method="get"> 
  <input type="text" name="username" placeholder="请输入用户名" required>
  <input type="password" name="psd" required> <br>
  <input type="submit" name="提交">
</form>
```
 比如上述代码就是一个输入用户名和密码以及提交按钮的form表单，点击提交按钮就会向action指向的地址发起对应method的HTTP方法。

input标签有很多的类型，比如text，password，submit, reset, radio, checkbox, button, image, file, url, email, number, range, search, pattern<br />分别是文本，密码，提交，重置，单选，多选，按钮，图像提交，上传文件的类型，输入URL的类型，输入邮箱的类型，数字，滑块进度，搜索，以及正则表达式匹配。

其他的知识点包括文本域 textarea，下拉框是select + option
```html
<form action="1.%20theFirstWeb.html" method="get">
<!--文本输入框：input type="text"
    value="你好" 默认初始值
    maxlength="8" 最长能写几个字符
    size="30" 文本框有多长
    readonly 只读
    disabled 禁用
    hidden   隐藏
    placeholder 提示作用
    required 必须
-->
  <p>账号 <input type="text" name="username" placeholder="请输入用户名" required></p>
  <p>密码 <input type="password" name="pwd" value="123456" disabled></p>
  <p>
    <input type="submit" name="提交">
    <input type="reset" name="重置">
  </p>
<!--单选框标签
    input type="radio"
    value : 单选框的值
    name ：表示一个组
-->
    <p>
        性别：
        <input type="radio" value="boy" name="sex" checked>男
        <input type="radio" value="girl" name="sex">女
    </p>
<!--多选框标签 checkbox-->
    <p>
        爱好：
        <input type="checkbox" value="sleep" name="hobby" checked>爱好
        <input type="checkbox" value="program" name="hobby">巧代码
        <input type="checkbox" value="chat" name="hobby">聊天
        <input type="checkbox" value="game" name="hobby">玩游戏

    </p>
<!--按钮
    button 普通按钮
    image  图片按钮
    submit 提交按钮
    reset  重置按钮
-->
    <p>
        按钮 <input type="button" name="btn1" value="点击变成"> <br>
        图片按钮 <input type="image" src="../resource/image/gopher.png" width="300px" height="300px">
    </p>

<!--多选下拉框 select 和 option-->
    <p>
        选择国家：
        <select name="country" >
            <option value="china">中国</option>
            <option value="united states">美国</option>
            <option value="india">印度</option>
            <option value="singapore" selected>新加坡</option>
        </select>
    </p>


<!--文本域 textarea-->
    <p>
        填写内容：<textarea name="content" cols="30" rows="5"></textarea>
    </p>
<!--文件域 上传文件 input的file-->
    <p>
        上传文件：
        <input type="file" name="files">
        <input type="submit">
    </p>
<!--邮箱是 input的email-->
    <p>邮箱：
        <input type="email" name="email">
    </p>
<!--URL 是input的url-->
    <p>URL：
        <input type="url" name="url">
    </p>
<!--数字是input的number-->
    <p>数字：
        <input type="number" name="num" max="100" min="0" step="9">
    </p>

<!--滑块 input的range-->
    <p>音量：
        <input type="range" name="voice" min="0" max="100" step="10">
    </p>
<!--搜索框 input的search-->
    <p>搜索：
        <input type="search" name="search">
    </p>
<!--label标签 增强鼠标的可用性 可指向-->
    <p>
        <label for="mark">你点我试试</label>
        <input type="text" id="mark">
    </p>
<!--input的pattern 正则表达式匹配-->
    <p>自定义邮箱：
        <input type="text" required pattern="^\w+([-+.]\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*$">
    </p>
</form>
```
