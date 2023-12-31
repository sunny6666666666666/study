# HTML NOTE
*2023.8.15*
## 01 基本概念
* HTML（Hyper Text Markup Language）超文本标记语言，在浏览器上运行。
* 超文本（超级文本）：如流媒体、声音、视频、图片等。
* 标记语言：由大量的标签组成。任何一个标签都有开始和结束标签。
  * <标签>：开始标签
  * </标签>：结束标签
* 世界5大主流浏览器：
  * IE 微软的(√)
  * FireFox 火狐(√)
  * Chrome 谷歌(√)
  * Opera 欧朋
  * Safari Mac OS 
* 新建一个.html或者.htm结尾的文件。使用记事本打开即可开发
* html不需要编译，语法不严格。
* html中的字符串可以使用单引号，也可以使用双引号。
* html不区分大小写。
## 02 web
web就是网站开发，web程序员包括web前端程序员和web后台程序员。
* web前端程序员需要精通：
  * html css javascript
  * 侧重前端浏览器展示的效果
* web后端程序员需要精通：
  * c / c++ / JAVA / PHP / Python等……
* 这种系统架构被称为B/S结构系统
  * B：Browser（浏览器）
  * S：Server（服务器）
## 03 HTML基本标签
``` html
<html>
      <head>
            <title>基本标签</title>
      </head>

      <body>
            <!--段落标记-->
      </body>
</html>
```
### 3.1 段落标记
分段标签，将文字分段。
``` html
<p>段落内容</p><p>段落内容</p>
```
### 3.2 标题字
一共有6个
``` html
<h1>标题字</h1>
<h2>标题字</h2>
<h3>标题字</h3>
<h4>标题字</h4>
<h5>标题字</h5>
<h6>标题字</h6>
```
### 3.3 换行标记
让hello world在中间换行，是独目标签。
``` html
hello <br> world
```
### 3.4 水平线
独目标签,其中color是标签的属性名，red是属性值。
``` html
<hr color="red">
```
### 3.5 预留格式
在html源码上是什么格式，到网页上还是这个格式不变。
``` html
<pre>
里面的内容可以保留原格式
</pre>
```
### 3.6 粗体字
``` html
<b>粗体字</b>
```
### 3.7 斜体字
``` html
<i>斜体字</i>
```
### 3.8 插入字
插入字下面会有下划线。
``` html
<ins>插入字</ins>
```
### 3.9 删除字
删除字对应文字部分有删除线。
``` html
<del>删除字</del>
```
### 3.10 右上角加字
想显示10的平方
``` html
<!--在右上角显示-->
10<sup>2</sup>
<!--在右下角显示-->
10<sub>2</sub>
```
### 3.11 font字体标签
``` html
<font color = "red" size = "5">hello</font>
```
## 04 HTML实体符号
windows操作系统默认情况下都是采用GBK的简体中文方式打开HTML页面的。因为我们的windows操作系统是简体中文操作环境。而程序员一般的编码方式是UTF-8的编码方式。所以在HTML页面中如果出现中文，那么就会出现乱码。所以我们需要告诉浏览器采用哪一种字符编码方式打开该页面。一般这个编码方式要和文件的编码方式相同，不然会乱码。
``` html
<font color = "red" size = "5">hello</font>
<!--HTML页面中第一行是以下代码的表示该页面是一个HTML5页面-->
<!DOCTYPE html>
<html>
      <head>
            <!--告诉浏览器采用哪一种字符编码方式打开该页面。一般这个编码方式要和文件的编码方式相同，不然会乱码。-->
            <meta charset="utf-8">
            <title>实体符号</title>
      </head>
      <body></body>
</html>
```
### 4.1 空格
``` html
<!--  &nbsp;  这是一个空格，属于实体符号-->
a&nbsp;bc
```
### 4.2 小于号 大于号
在html中，小于号和大于号有特殊的含义，所以不能直接使用，需要使用实体符号。

``` html
<!-- &lt;这是小于号-->
<!-- &gt;这是大于号-->
```
## 05 表格
### 5.1 基本内容
![Alt text](image.png)
如上图所示，对于一个表格table，每一行为tr，每一行中的一列为td。
``` html
<!DOCTYPE html>
<html>
      <head>            
            <meta charset="utf-8">
            <title>实体符号</title>
      </head>
      <body>
            <!-- 3行3列的table-->
            <!-- border用来设置边框的宽度，1px代表1像素-->
            <!-- 表格的宽度和高度还可以设置为百分比模式，在这种情况下，表格的宽度随网页的缩放动态缩放-->
            <!-- align设置表格居中-->
            <table border="1px" width="50%" height="200px" align=“center”>
                  <tr>
                        <td>姓名</td>
                        <td>年龄</td>
                        <td>性别</td>
                  </tr>
                  <tr>
                        <td>张三</td>
                        <td>18</td>
                        <td>男</td>
                  </tr>
                  <tr>
                        <td>李四</td>
                        <td>19</td>
                        <td>女</td>
                  </tr>
            </table>
      </body>
</html>
```
### 5.2 单元格的合并
同一行两个单元格合并叫列合并，需要删除一个单元格，然后在另一个单元格中使用colspan属性，合并几个就写几个。  
1.例如想合并第一行中的第2个和第3个单元格，代码如下所示。
``` html
<!DOCTYPE html>
<html>
      <head>            
            <meta charset="utf-8">
            <title>表格列合并</title>
      </head>
      <body>            
            <table border="1px" width="50%" height="200px" align=“center”>
                  <tr>
                        <td>姓名</td>
                        <td colspan="2">年龄性别</td>
                        <!--<td>性别</td>-->
                  </tr>
                  <tr>
                        <td>张三</td>
                        <td>18</td>
                        <td>男</td>
                  </tr>
                  <tr>
                        <td>李四</td>
                        <td>19</td>
                        <td>女</td>
                  </tr>
            </table>
      </body>
</html>
```
2.例如想合并第3列中的第2行和第3行单元格，代码如下所示。删除下面的第3行，然后在第2行中使用rowspan属性，合并几个就写几个。
``` html
<!DOCTYPE html>
<html>
      <head>            
            <meta charset="utf-8">
            <title>表格行合并</title>
      </head>
      <body>            
            <table border="1px" width="50%" height="200px" align=“center”>
                  <tr>
                        <td>姓名</td>
                        <td colspan="2">年龄</td>
                        <td>性别</td>
                  </tr>
                  <tr>
                        <td>张三</td>
                        <td>18</td>
                        <td rowspan="2">男女</td>
                  </tr>
                  <tr>
                        <td>李四</td>
                        <td>19</td>
                        <!--<td>女</td>-->
                  </tr>
            </table>
      </body>
</html>
```
### 5.3 th标签
th可以代替td。用来表示表格的标题，th标签的内容默认是居中的，加粗的。
``` html
<!DOCTYPE html>
<html>
      <head>            
            <meta charset="utf-8">
            <title>th标签</title>
      </head>
      <body>            
            <table border="1px" width="50%" height="200px" align=“center”>
                  <tr>
                        <td>姓名</td>
                        <td>年龄性别</td>
                        <td>性别</td>
                  </tr>
                  <tr>
                        <td>张三</td>
                        <td>18</td>
                        <td>男</td>
                  </tr>
                  <tr>
                        <td>李四</td>
                        <td>19</td>
                        <td>女</td>
                  </tr>
            </table>
      </body>
</html>
```
### 5.4 thead、tbody、tfoot标签
thead表示表格的头部，tbody表示表格的主体，tfoot表示表格的尾部。可以方便后期使用JS操作表格更加方便简洁一些。
``` html
<!DOCTYPE html>
<html>
      <head>            
            <meta charset="utf-8">
            <title>thead、tbody、tfoot标签</title>
      </head>
      <body>            
            <table border="1px" width="50%" height="200px" align=“center”>
               <thead>
                  <tr>
                        <td>姓名</td>
                        <td>年龄性别</td>
                        <td>性别</td>
                  </tr>
               </thead>  
               <tbody>
                  <tr>
                        <td>张三</td>
                        <td>18</td>
                        <td>男</td>
                  </tr>
                  <tr>
                        <td>李四</td>
                        <td>19</td>
                        <td>女</td>
                  </tr>
               <tbody>  
               <tfoot>
                  <tr>
                        <td>李四</td>
                        <td>19</td>
                        <td>女</td>
                  </tr>
               </tfoot>
            </table>
      </body>
</html>
```
## 06 背景颜色和背景图片
### 6.1背景颜色
``` html
<html>
      <head>
            <title>背景颜色</title>
      </head>
      <!--body标签的bgcolor-->
      <body bgcolor="red">
            
      </body>
</html>
```
### 6.2背景图片
body标签的background属性用于指定背景图片
``` html
<html>
      <head>
            <title>背景图片</title>
      </head>
      
      <body background="图片路径"></body>
</html>
```
## 07 图片
``` html
<html>
      <head>
            <title>图片</title>
      </head>
      
      <body>
            <img src="图片路径"></img>
           <!--开始标签和结束标签之间没有内容的话，可以直接把结束标签删除掉，开始标签末尾添加 / --> 
           <img src="图片路径"/>
      </body>
</html>
```
### 7.1图片的属性
src属性用来指定图片的路径
width属性用来指定图片的宽度，高度会等比例缩放（不要手动设置高度）
title属性用来指定鼠标悬停在图片上时显示的文字（提示信息）
alt属性用来指定图片加载失败时显示的文字（替换文字）
``` html
<html>
      <head>
            <title>图片</title>
      </head>
      
      <body>
            <img src="图片路径" width="200px" title="提示信息"></img>         
      </body>
</html>
```
## 08 超链接
链接的可以是一个网址，也可以是一个本地文件的路径。
超链接的特点，鼠标悬停在超链接上时，鼠标会变成小手的形状，超链接自动添加下划线。
``` html
<html>
      <head>
            <title>超链接</title>
      </head>     
      <body>
            <!--链接到百度-->
            <a href="http://www.baidu.com">链接到百度</a>
            <!--链接到本地的表格-->
            <a href="004-表格.html">链接到本地的表格</a>  
            <!--图片也可以做成超链接-->   
            <a href="http://www.baidu.com">
                  <!--标签嵌套使用-->
                  <img src="图片路径" width="200px" title="提示信息"></img>
            </a>     
      </body>
</html>
```
### 8.1超链接的target属性
target属性用来设置最终打开窗口的位置。
![Alt text](image-1.png)
``` html
<html>
      <head>
            <title>超链接的target属性</title>
      </head>     
      <body>
            <!--链接到百度，当前窗口打开-->
            <a href="http://www.baidu.com" target=“_self”>链接到百度（当前窗口打开）</a> 
            <!--链接到百度，新窗口打开-->
            <a href="http://www.baidu.com" target=“_balnk>链接到百度（新窗口打开）</a>
      </body>
</html>
```