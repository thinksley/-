## 前端开发规范

### 适用范围
适用于前端，移动端开发人员。
##### 术语
###### HTML：是英文HyperTextMarkupLanguage的缩写，中文意思是“超文本标志语言”，用它编写的文件(文档)的扩展名是.html或.htm，它们是可供浏览器解释浏览的文件格式。
###### HTML5：HTML5是HTML最新的修订版本，2014年10月由万维网联盟（W3C）完成标准制定。
CSS: 层叠样式表(英文全称：Cascading Style Sheets)是一种用来表现HTML或XML（标准通用标记语言的一个子集）等文件样式的计算机语言。
###### JAVASCRIPT: JavaScript一种直译式脚本语言，是一种动态类型、弱类型、基于原型的语言。
###### VUE: vue.js是一个构建数据驱动的 web 界面的渐进式框架。Vue.js 的目标是通过尽可能简单的 API 实现响应的数据绑定和组合的视图组件。它不仅易于上手，还便于与第三方库或既有项目整合。

### 1. HTML部分
##### <font color="1e90ff">1.1 语法</font>
1.	缩进使用soft tab（4个空格）；
2.	嵌套的节点应该缩进；
3.	在属性上，使用双引号，不要使用单引号；
4.	属性名全小写，用中划线做分隔符；
5.	自动闭合标签结尾处使用斜线自闭合标签；
6.	不要忽略可选的关闭标签；

##### <font color="1e90ff">1.2 HTML5 DOCTYPE</font>

HTML文件必须加上 DOCTYPE 声明，并统一使用 HTML5 的文档声明。

例子：[![](http://wiki.paohe.cn/uploads/images/gallery/2020-10/scaled-1680-/image-1603094841902.png)](http://wiki.paohe.cn/uploads/images/gallery/2020-10/image-1603094841902.png)
##### <font color="1e90ff">1.3 lang属性</font>

根据HTML5规范，应在html标签上加上lang属性。这会给语音工具和翻译工具帮助，告诉它们应当怎么去发音和翻译。

例子：
[![
![](media/7c64270d9c031595bd648d297fad53cc.png)](http://wiki.paohe.cn/uploads/images/gallery/2020-10/scaled-1680-/image-1603095131583.png)](http://wiki.paohe.cn/uploads/images/gallery/2020-10/image-1603095131583.png)

##### <font color="1e90ff">1.4 字符编码</font>

让浏览器快速的确定适合网页内容的渲染方式，默认指定为'UTF-8'。


##### <font color="1e90ff">1.5 IE兼容模式</font>

用 \<meta\> 标签可以指定页面应该用什么版本的IE来渲染。


##### <font color="1e90ff">1.6 移动端META标准开头</font>

手机端添加meta头告诉浏览器适配屏幕显示。

-   width – viewport的宽度

-   height – viewport的高度

-   initial-scale – 初始的缩放比例

-   minimum-scale – 允许用户缩放到的最小比例

-   maximum-scale – 允许用户缩放到的最大比例

-   user-scalable – 是否允许用户缩放

##### <font color="1e90ff">1.7引入CSS,JS</font>

根据HTML5规范, 通常在引入CSS和JS时不需要指明
type类型，一般浏览器会默认类型为text/css和text/javascript。

##### <font color="1e90ff">1.8 属性顺序</font>

标签属性应该按照特定的顺序出现以保证易读性；

id

class

name

data-\*

src type href value

placeholder title alt

required readonly disabled

##### <font color="1e90ff">1.9 减少标签数量</font>

在编写HTML代码时，需要尽量避免多余的父节点。尽量减少html节点的层次。尽量避免在js里渲染html标签，在JS文件中生成标签会让内容变得更难查找，更难编辑，性能更差，而且维护和可读性性较差，应该尽量避免这种情况的出现。



### 2. CSS/LESS/SASS部分
##### <font color="1e90ff">2.1 缩进</font>
使用soft tab（4个空格）。

##### <font color="1e90ff">2.2 分号</font>
每个属性声明末尾都要加分号。
##### <font color="1e90ff">2.3 空格</font>
以下几种情况不需要空格：
•	属性名后；
•	多个规则的分隔符逗号前；
•	属性值中'('后和')'前；
•	行末不要有多余的空格；
•	以下几种情况需要空格；
•	属性值前；
•	选择器'>', '+', '~'前后；
•	'{'前；
•	!important '!'前；
•	属性值中的','后；
•	注释'/*'后和'*/'前；

 
以下几种情况需要空行：
写css文件的时候每个属性只占一行，不连在一行。

 
##### <font color="1e90ff">2.4 !important</font>
禁止使用!important。!important 拥有最高的优先级，是人为的强制重置，由于其具有较高的灵活性，使用时要考虑是否会对其他的样式产生影响，该规则在ie6下有浏览器级别的bug，使用!important对于性能并没有什么负面影响，但是从可维护性角度考虑还是少用这个规则，可通过增加选择器权重来达到覆盖样式的目的。
##### <font color="1e90ff">2.5 注释</font>
css/less/sass/styls 里的注释统一用'/* */'。

 
##### <font color="1e90ff">2.6 引号</font>
•	最外层统一使用双引号；
•	url的内容要用引号；
•	属性选择器中的属性值需要引号；（注意：禁止属性用单引号）
##### <font color="1e90ff">2.7 颜色</font>
•	颜色16进制用小写字母；
•	颜色16进制尽量用简写；

##### <font color="1e90ff">2.8 命名</font>
•	使用小写字母，以中划线分隔；
•	scss中的变量、函数、混合、placeholder采用驼峰式命名；
•	id名使用驼峰；
•	某元素需要被jquery获取的时候前面类名或id名 前面加“ J_ ” ，目的在于告诉别该元素被js用到了，利于阅读；

 
##### <font color="1e90ff">2.9 其他</font>
•	不允许只写属性名不写属性值的情况；
•	元素选择器用小写字母；
•	去掉小数点前面的0；
•	去掉数字中不必要的小数点和末尾的0；（例如：.7px 不要写成 0.7px）
•	属性值'0'后面不要加单位；（注意：不要写 0px， 0em）
•	不要在一个文件里出现两个相同的规则；
•	选择器不要超过4层（在scss中如果超过4层应该考虑用嵌套的方式来写）；
•	css文件中不要有 @important;
•	禁止使用'*'选择器；（例如：禁止*{margin:0;padding:0}）
##### <font color="1e90ff">2.10 外部cdn样式库的引用</font>
禁止引用外部cdn的第三方css库，错误做法:
<link href=“http://libs.baidu.com/css/css.css”/>
正确做法:将第三方库下载到本地工程，从本地工程中引入第三方库。

##### <font color="1e90ff">2.11 CSS书写顺序</font>
单个样式规则下的属性在书写时以 布局方式，位置> 盒模型 > 文字排版> 视觉外观 的顺序书写，按功能进行分组，组之间需要有一个换行隔开，以提高代码的可读性。
1.	布局方式、位置，相关属性包括：position, top, z-index, display, float等
2.	盒模型，相关属性包括：width, height, padding, margin，border,overflow
3.	文本排版 相关属性包括：font-size, line-height, text-align,vertical-align
4.	视觉外观，相关属性包括：color, background, list-style, transform, animation
 	工具使用：在vscode里面添加插件：“PostCSS Sorting”，将上述的顺序写入插件配置即可实现自动排序
    
    
### 3. JAVASCRIPT部分

##### <font color="1e90ff">3.1 缩进</font>

使用soft tab（4个空格）。

##### <font color="1e90ff">3.2 分号</font>

需加分号：

-   变量声明

-   表达式

-   return

-   throw

-   break

-   continue

-   do-while

##### <font color="1e90ff"> 3.3 空格</font>

不需要空格：

-   对象的属性名后

-   前缀一元运算符后

-   后缀一元运算符前

-   函数调用括号前

-   无论是函数声明还是函数表达式，'('前不要空格

-   数组的'['后和']'前

-   对象的'{'后和'}'前

-   运算符'('后和')'前

需要空格：

-   二元运算符前后

-   三元运算符'?:'前后

-   代码块'{'前

-   下列关键字前：else while catch finally

-   下列关键字后：if else for while do switch case try catch finally return
    typeof

-   单行注释'//'后（若单行注释和代码同行，则'//'前也需要），多行注释'\*'后

-   对象的属性值前

-   for循环，分号后留有一个空格，前置条件如果有多个，逗号后留一个空格

-   无论是函数声明还是函数表达式，'{'前一定要有空格

-   函数的参数之间

##### <font color="1e90ff"> 3.4 空行</font>

需要空行：

-   变量声明后（当变量声明在代码块的最后一行时，则无需空行）；

-   注释前（当注释在代码块的第一行时，则无需空行）；

-   代码块后（在函数调用、数组、对象中则无需空行）；

-   文件最后保留一个空行；

##### <font color="1e90ff"> 3.5 单行注释</font>

-   双斜线后，必须跟一个空格；

-   缩进与下一行代码保持一致；

-   可位于一个代码行的末尾，与代码间隔一个空格；

##### <font color="1e90ff">3.6 多行注释</font>

最少三行, '\*'后跟一个空格。建议在以下情况下使用：

-   难于理解的代码段；

-   可能存在错误的代码段；

-   浏览器特殊的HACK代码；

-   业务逻辑强相关的代码；

-   针对某个函数的说明和参数描述；

##### <font color="1e90ff"> 3.7 引号</font>

统一使用单引号。

##### <font color="1e90ff">3.8 变量命名</font>

-   标准变量采用驼峰式命名（除了对象的属性外，主要是考虑到cgi返回的数据）

-   'ID'在变量名中全大写

-   'URL'在变量名中全大写

-   'Android'在变量名中大写第一个字母

-   'iOS'在变量名中小写第一个，大写后两个字母

-   常量全大写，用下划线连接

-   构造函数，大写第一个字母

-   jquery对象必须以'\$'开头命名

##### <font color="1e90ff"> 3.9 函数</font>

-   无论是函数声明还是函数表达式，'('前不要空格，但'{'前一定要有空格；

-   函数调用括号前不需要空格；

-   立即执行函数外必须包一层括号；

-   参数之间用', '分隔，注意逗号后有一个空格。


##### <font color="1e90ff">3.9 数组，对象</font>

-   对象属性名不需要加引号；

-   对象以缩进的形式书写，不要写在一行；

-   数组、对象最后不要有逗号；

##### <font color="1e90ff">3.10 等于号的使用</font>

所有的if判断用三个等于号 “ ===” ；

不使用两个等于号 ；

##### <font color="1e90ff"> 3.11 不等于号的使用</font>

用“!==”代替“!=”

##### <font color="1e90ff">3.12 小于等于，大于等于号的使用</font>

用“\<==”代替“\<=”；

用“\>==”代替“\>=”；

##### <font color="1e90ff"> 3.13 undefined</font>

不要直接使用undefined进行变量判断；

请使用typeof和字符串'undefined'对变量进行判断。

  ##### <font color="1e90ff">3.14 外部cdn地方三库的引用</font>

禁止引用外部cdn的第三方js库，错误做法:

\<script src="http://libs.baidu.com/jquery/1.9.0/jquery.js"\>\</script\>

正确做法:将第三方库下载到本地工程，从本地工程中引入第三方库


### 4. 图片部分

-   图标大小不超过10kb；

-   网页单个图片大小控制在50k\~100k之间；

-   图片格式如果不是内容发布后台输出的，一律使用png-24导出的png格式图片，或gif图片；

-   传统jquery项目中图标必须使用css精灵合并，vue项目中自动打包成base64；

-   使用字体图标；

   
   
### 5. VUE项目部分

##### <font color="1e90ff"> 5.1 缩进法</font>

使用soft tab（4个空格）。

##### <font color="1e90ff"> 5.2 样式文件存放位置法</font>

样式文件名跟组件名保持一致，目录结构保持跟页面级目录文件夹一致，方便维护和查看。

##### <font color="1e90ff"> 5.3 分号的使用法</font>

除了样式每个属性后面需要添加分号外，js部分里不以分号结尾。

##### <font color="1e90ff"> 5.4 目录命名法</font>

源代码目录放在src目录下，目录名称采用英文小写，目录名称应做到简介明了，一眼能看出该文件夹存放的内容是干什么事。

##### <font color="1e90ff"> 5.5 eslint的使用法</font>

eslint在vue-cli脚手架中作为可选方案，建议开启，并在对应的编辑器里安装eslint检测插件。

##### <font color="1e90ff"> 5.6 组件文件夹命名法</font>

以大驼峰方式命名文件夹名称。


##### <font color="1e90ff"> 5.7 组件法</font>

组件名以小驼峰命名

##### <font color="1e90ff"> 5.8 Vue组件的书写顺序法</font>

按照 template script style 的顺序书写

##### <font color="1e90ff"> 5.9 组件引用法</font>

##### <font color="1e90ff"> 5.10 事件绑定方法</font>

