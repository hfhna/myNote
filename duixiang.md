# 对象
> 客观的事物，抽象的规则 ，计划 ，事件
> 属性的无序集合体

        * 属性  值普通的数据类型的时候
        * 方法  值为函数
## 类
        * 类是具有相同或者相似属性的对象的抽象描述，类的具体化 或者 实例化 就是对象
        * 在javascript中是 通过构造函数实现类的定义的
        * new 实例化构造函数 得到对象
##  对象的分类
    * 本地对象
        * 内置对象
            * Math 数学对象
            * 全局对象   window
        * Array()
        * String()
        * Function()
        * Boolean()
        * Number()
        * RegExp()  正值对象
        * Date()
    * 宿主对象
        * BOM  浏览器对象模型
            * history
            * loaction
            * navigater
        * DOM  文档对象模型
            * document 对象
            * 其他标签元素
* 对象的声明/创建
    * JSON javascript 原生对象描述法
    * 自己定义构造函数  通过实例化构造函数得到对象
    * 实例化 Object
* 对象属性的添加
  > 属性名  英文单词 属性值，可以是任意的数据类型
    * 创建的时候直接添加
        * var obj={name:"zhangsan",age=17}
        > 属性之间用，隔开
         属性和值可以用一个变量表示
        * function Phone(){
            this.name="zhangsan"
        }
    * 创建之后添加
        * 对象.属性=值
        * 对象[变量]=值
* 对象属性的访问
    * 对象.属性
    * 对象.方法（）
    * 对象[变量]
    * 遍历  for(var i in obj){ console.log(obj[i])}
* 对象属性的删除
    * delete 对象.属性
    * delete 对象[变量]
    * delete 对象.方法
* instanceof 判断某个对象是否是由某个构造函数实例化的结果
* constructor属性  当前对象的构造函数
* 清空对象
    * obj=null
    * 留在内存当中 javascript垃圾回收机制会在某一个时刻从内存中彻底删除这个对象

## 继承
    * 在javascript当中，每一个对象都会自动获得另一个对象所有的属性和方法。
    这种行为称为继承，被继承的对象称为当前对象的原型
    * 继承实现的方式有两种
        * 第一种方式  通过指定当前对象的构造函数的prototype值为原型对象，就能实现继承
        * 第二种方式  对象冒充

## this
> 在每一个函数里面都有的
* 当函数为构造函数的时候，this指的就是当前构造函数实例化的对象
* 在一般函数当中，this指的是window对象
* 在作为方法的函数当中，this指的是调用这个方法的对象
* 当函数在调用的时候使用 call apply 调用的时候 ，this指的是传入的第一个参数
> call apply 传递其他参数的时候，如果使用call 在后面继续写参数 ，
如果是apply 把参数放置到一个数组当中传入

* console.dir()   输出一个对象的详细信息
* console.table()   以表格的形式输出
* cursor：pointer（手形）  crosshair(十字)  help（箭头+问号） move  ne-resize  e-resize  wait（等待）  css中设置鼠标样式
* document.querySelector()

# 数组对象

## ECMAScript3

 |方法|参数|返回值|功能|
 |:----:|:----:|:----:|:----:|
 |push|一个或者多个元素|新数组的长度|在数组的末尾添加|
 |pop|无|被删除的元素|在数组的末尾删除|
 |unshift|一个或者多个元素|新数组的长度|在新数组开始的位置添加|
 |shift|无|被删除的元素|在新数组开始的位置删除|
 |splice|1：位置 2:删除的个数之后都是要添加的元素|被删除元素组成的数组|万能的添加 删除 替换方法|
 |join|连接符|转换之后的字符串|将数组转换为字符串|
 |slice|位置 一个参数表示从当前位置到结束 俩个参数就是选中的范围|截取到的数组|从数组中截取一段组成新数组|
 |sort|回调函数|排序之后的数组|对数组排序|
 |concat|要被拼接的数组|拼接后的新数组|数组的拼接|

##ECMAScript5
|方法|参数|返回值|功能|
|:----:|:----:|:----:|:----:|
|forEach|callback|undefined|遍历数组中的每一个数|
|filter|callback|arr|过滤数组|
|map|callback|arr|映射新数组|
|some|callback|boolean|判断数组当中是否有符合条件的元素|
|every|callback|boolean|判断数组当中每一个是否都符合条件|
|indexOf|item|number|返回数组当中 某个元素第一次出现的位置|
|lastIndexOf|item|number|返回数组当中某个元素最后一次出现的位置|
|reduce|callback，init|*|对数组当中每个元素从左到右进行累加操作|
|reduceRight|callback,init|*|对数组当中每个元素从右到左进行累加操作|
|reverse|无|arr|将数组当中元素的顺序颠倒|

##ECMAScript6
|方法|参数|返回值|功能|
|:----:|:----:|:----:|:----:|
|find|callback|item|在数组中找到某个值并取出 找不到undefined|
|findIndex|callback|index|在数组中找到某个值得位置并返回|
|copyWithin|1:目标位置 2：复制的开始位置 3：复制的结束位置|undefined|从数组当中复制一段放置到另一个位置|
|fill|1:填充的内容 2，3：填充的起始位置和结束位置|arr|快速填充指定长度的空数组|
|includes|item|boolean|判断数组当中是否有某个元素|

# 字符串对象
## 属性
    * length  字符串的长度
    * [] 访问到字符串当中对应下标的值
    * constructir 访问构造函数
## 方法
> 按照功能类型来分类
* 获取

|方法|参数|返回值|功能|
|:----:|:----:|:----:|:----:|
|charAt|number|string|获取指定位置的字符串|
|charCodeAt|number|number|获取指定位置字符串的ASCII码|
|String.fromCharCode|number+|string|根据指定的一个或者多个ASCII码 得到对应的字符串|
* 查找

|方法|参数|返回值|功能|
|:----:|:----:|:----:|:----:|
|indexOf|string|number|查找某个字符串在当前字符串当中第一次出现的位置|
|lastIndexOf|string|number|查找某个字符串在当前字符串当中最后一次出现的位置|
|replace|str1,str2|string|查找到字符串当中的str1并替换为str2|
|includes|str|boolean|判断当前字符串当中是否包含某个字符串|
|startsWith|str|boolean|判断当前字符串是否是以某个字符串开始的|
|endsWith|str|boolean|判断当前字符串是否是以某个字符串结束的|

* 截取
    * slice 和数组一样
    * substring 与slice的区别 不能传负值
    * substr  截取指定位置指定长度的字符串
* 转换
    * toLowerCase
    > 将大写字母转换为小写字母
    * toUpperCase
    > 将小写字母转换为大写字母
    * split
    > 将字符串抓换为数组 第一个参数分隔符 第二个参数最大长度
* trim
> 去除字符串两端的空格

# Math 对象
> 不需要实例化的内置对象

|方法|参数|
|:----:|:----:|
|Math.abs()|取绝对值|
|Math.round()|四舍五入取整|
|Math.floor()|向下取整|
|Math.ceil()|向上取整|
|Math.max()|取最大值|
|Math.min()|取最小值|
|Math.random()|取随机数|
|Math.pow(x,y)|求x的y次幂|
|Math.sqrt()|求平方根|
|Math.sin()|求正弦值|
|Math.con()|求余弦值|
|Math.tan()|求正切值|
|Math.PI|π值|
* 任意的随机数
> Math.random()*范围+最小值
* 角度和弧度的转换
> 角度*Math.PI/180

# 解构赋值（ES6）
> 根据特定的匹配模式，从数组或者对象当中提取值给变量赋值的一种形式
* 数组的解构赋值
    * 基本用法  两边的模式匹配就可以完成赋值；
~~~javascript
    var [a,b,c]=[1,2,3];//1 2 3
    var [a,[b],c]=[1,[2],3] //1 2 3
~~~

    * 空值的处理 使用的变量可以是空值,赋的值也可以是空值 会自动赋值为undefined
~~~javascript
    var [a,b]=[1,2,3] //左边有空值 1 2
    var [,a,b]=[1,2,3]//2 3
    var [a,b,c]=[1,2]//右边有空值 1 2 undefined
    var [a,b,c]=[,2,3]//undefined 2 3
 ~~~
    * 默认值 变量可以通过=添加默认值，如果在赋值表达式的右侧没有对应值或者对应值为undefined 则会是由默认值
 ~~~javascript
     var [a=1,b]=[,2];//1 2
     var [a=1,b=2]=[,3] //1 3
 ~~~
    * 结合扩展运算符，可以完成对于数组的赋值 被扩展的变量只能是最后一个变量
~~~javascript
     var [a,...b]=[1,2,3,4,5]//1 [2,3,4,5]
~~~

* 对象的解构赋值
~~~javascript
    var obj={myname:"zhangsan",myage:17};
    var {myname,myage}=obj;
    console.log(myname,myage);  //"zhangsan"  17
    var {myname:n,myage:a}=obj;
    console.log(n,a);//"zhangsan"  17
~~~
* ...  扩展运算符
> 将可遍历的结构（arr str document.quertySelectorAll（）） 转化为序列化的参数形式
* toFixed(n)
> 对数值保留n位小数的方法

# DOM
> 文档对象模型
## document
    * 属性
        * URL 当前页面的地址
        * body 获取到body标签
        * head 获取到head标签
        * title 当前title的内容
        * all   获取所有的标签元素
        * images  获取所有图片元素集合
        * forms   获取所有的form表单对象集合
        * links   获取所有的链接集合

    * 方法
        * querySelector()
        > 通过传递一个选择器获取到某一个元素对象，如果选择器能选中很多个，会选中第一个，选择不到会得到null
        * querySelectorAll()
        > 通过传递一个选择器获取到某一个元素对象集合，如果只能获取到一个，也是一个集合，如果选择不到，会得到一个空集合
        * getElementsByClassName()
        > 通过传递一个类名获取到某一个元素对象集合，如果只能获取到一个，也是一个集合，如果选择不到，会得到一个空集合
        * getElementsByTagName()
        > 通过传递一个标签名获取到某一个元素对象集合，如果只能获取到一个，也是一个集合，如果选择不到，会得到一个空集合
        * getElementById()
        > 通过传递一个id获取到某一个元素对象，如果获取不到得到null
## 普通的元素对象  (div p a)
    * innerHTML  获取或者设置内容
    * textContent  获取或者设置文本内容  不识别标签
    * style     获取或者设置行内样式集合
    * value     获取或者设置表单元素的value
    * id      获取或者设置元素的id值
    * className   获取或者设置元素的类名
    * classList  对象  包含类名信息
        * add()  给元素添加一个类名
        * remove()  从元素对象身上移出一个类名
        * toggle()  切换某一个元素类名的添加移出状态
        * contains() 判断是否包含某个类名
* 方法
    * addEventListener()  用来给元素添加事件的
    * querySelector()
    * querySelectorAll()
    * offsetWidth  一个元素在页面当中所占的实际宽度
    * offsetHeight   一个元素在页面当中所占的实际高度
    * offsetLeft
    * offsetTop
    > 如果前辈元素没有定位属性  offsetLeft offsetTop 相对于文档的坐标 ，如果前辈元素有定位属性，就是相对于前辈元素的坐标
    * scrollLeft
    * scrollTop
    * 兼容性的获取当前的可视窗口
    > obj=document.body.scrollTop==0?document.documentElement:document.body;
* 事件
> 用户对页面所做的一些操作或者是浏览器自身的一些行为

      * onclick
      * ondblclick  双击事件
      * onmousedown  鼠标按下
      * onmouseup   鼠标抬起
      * onmouseover
      * onmouseout
      * onmousemove 鼠标移动事件 ，只要鼠标移动，一直触发
      * onfocus  获得焦点 （表单）
      * onblur   失去焦点  （表单）
      * onscroll  当某个元素或者页面的滚动条位置发生改变的时候触发的事件

* 获取元素css属性的方法(在任何地方设置的 包括默认值)
    * getComputedStyle(div),width
## 获取浏览器宽高
     * documentElement.clientWidth
     * documentElement.clientHeight
     * window.innerWidth
     * window.innerHeight

## 节点
    * 每一个标签都是一个节点
    * 每一个文本内容是一个节点
    * 每一个标签的属性也是一个节点
    * 注释也是节点
    * document整个文档也是一个节点
    * 属性
        * 实现节点之间的互相访问
          * parentNode  访问父节点
          * childNodes  访问子节点集合
          * firstChild 访问第一个子节点
          * lastChild  访问最后一个子节点
          * nextSibling  访问下一个兄弟节点
          * previousSibling  访问上一个兄弟节点
          * nextElementSibling  访问下一个元素兄弟节点
        * 每一个节点的信息属性
           * nodeType
           * nodeName
           * nodeValue

   |节点|nodeType|nodeName|nodeValue|
   |:----:|:-----:|:----:|:----:|
   |元素节点|1|大写的标签名|null|
   |属性节点|2|属性名|属性值|
   |文本节点|3|#text|文本的内容|
   |注释节点|8|#comment|注释的内容|
   |document节点|9|#document|null|
    * 节点的方法
        * 创建一个元素
        > document.creatElement("div")
        * 插入到页面
        > document.body.appendChild()   插入到元素之后
        > ele.insertBefore(新元素，被插入的元素) 插入到元素之前
        * 删除一个元素
        > ele.removeChild(被删除的元素)  ele是要删除元素的父元素
        * 替换一个元素
        > ele.replaceChild(新元素，被替换的元素)
        * 克隆节点
        > cloneobj=obj.cloneNode()
        > 传入参数true  表示也要克隆子节点


## ES6新增的数据类型
    * Symbol（）  独一无二的

## ES6 语法
    class Human{
        constructor(name){
            this.name=name;
            this.arm=2;
            this.leg=2;
        }
    }
    class Student extends Human{
        constructor(classNum,number,name){
            super(name);
            this.classNum=classNum;
            this.number=number;
        }
        say(){
            alert(1)
        }
    }

# set 和 map
 > 两个特殊的对象

 ## set
 > 类似于数组 只不过当中保存的都是不重复的值
 * new Set()
 * size 内容的个数
 * add() 添加内容   返回值是对象本身所有可以链式调用
 * delete() 删除某一个内容   返回值是是否删除成功  true/false;
 * has()  返回值是否包含某一个内容
 * forEach() 进行遍历
 * entries() keys() values()   提供给for...of...  进行遍历
 ## map
 > 类似于对象 只不过属性名可以是任意类型的值
 * set(属性名，属性值)  添加
 * get(属性名)   传一个属性名就可以得到属性值
 * clear()  清空所有的内容
 * delete()  进行删除
 * forEach()  进行遍历
 * has()   进行判断

# BOM
> 浏览器对象模型

* window
    * 属性
        * window.innerWidth
        * window.innerHeight
        > 获取浏览器的分辨率
        * window.screen.width
        * window.screen.height
        * window.screenLeft    IE  chrome
        * window.screenX    ff chrome
        * window.screenTop
        * window.screenY
        * top  当前页面的顶层窗口的window对象  iframe
    * 方法
        * alert()
        * prompt()
        * confirm()  带有提示信息的确认窗口  可以点击确认或者取得
        * setInterval()
        * setTimeout()
        * clearInterval()
        * clearTimeout()
        * getComputedStyle()  获取css属性
* history
    * 属性
        * length  表示当前历史记录的条数
    * 方法
        * forward() 跳转到历史记录的下一条
        * back()  跳转到历史记录的上一条
        * go()  1 下一条  -1  上一条  0  刷新页面
* location   地址栏对象
> 保存地址的各种细节
~~~html
    http://   协议
    locahost    域名   127.0.0.1
    ：63342//  端口号
    /WUIF1612/4.22/2.html   路径
    ?zh=123456  查询字符串
    #top  锚链接地址
~~~
    * location.protocol  访问协议
    * location.hostname   访问域名
    * location.host   域名+端口号
    * location.port   访问端口号
    * location.origin   协议+域名+端口号
    * location.pathname  访问路径
    * location.search  查询部分
    * location.hash  锚链接地址
    * location.href   访问整个路径
    * location.reload()   刷新网页
    * location.assign("http://www.baidu.com")  跳转到指定地址
    * location.replace("http://www.baidu.com")  跳转到指定地址  不会留下历史记录


# 事件对象
   ## 事件：用户对于浏览器的一些操作或者是浏览器自身的一些行为。
    * onclick  onmouseover onmouseout
    * ondblclick onmousedown onmouseup onmousemove
    * onfocus onblur
    * onkeydown onkeyup onkeypress
    * onload
  ## 事件的添加
     1. on+事件名
     2.添加事件监听
        * addEventListener("事件名称"，事件处理程序)   现代浏览器
        * attachEvent("on"+事件名称，事件处理程序)   ie8以下
  ## 事件的移除
     * removeEventListener(事件名称，事件处理程序)
     * detachEvent（）
  ## 一般对于兼容性的处理方案
    * 写一个函数
        document.documentElement.scrollTop!=0?document.documentElement:document.body;
    * 判断在什么浏览器当中
    * 执行各自对应的操作
~~~javascript
    function addEvent(obj,event,callback) {
      if(window.addEventListener){
        obj.addEventListener(event,callback);
      }else{
        obj.attachEvent("on"+event,callback);
      }
    }
~~~
  ## 事件对象
  > 在事件发生的时候，产生的一系列关于事件触发详细情况的一个对象
  * e.screenX e.screenY  鼠标点击位置 距离屏幕左上角的坐标
  * e.clientX e.clientY   距离浏览器窗口 左上角的坐标
  * e.pageX e.pageY    距离文档 左上角的坐标
  * e.offsetX e.offsetY   距离事件源左上角的坐标
  * e.keyCode  当前所按键的键盘码  如果同时有多个键被按下，那就是最后所按键的键盘码
  * e.ctrlKey  e.shiftKey   e.altKey  判断某一个键是否是被按下的状态
  ## 事件流
  > 当某个元素身上的事件触发的时候，整个页面以及元素所有的前辈元素都会按照特定的方式响应这个事件，这种事件传播的流程就称之为事件流
  ### 冒泡型事件流
  > 默认存在在任何一个事件当中
  > 触发顺序  从最明确的事件源到最不明确的事件源（从小到大）依次触发

  ### 捕获型事件流
  > addEventListener(event,fn,true)   才会触发捕获型事件流
  > 触发顺序  从最不明确的事件源到最明确的事件源依次触发
  > 捕获型事件流触发完成之后，依然还会触发冒泡

  ### 事件流的利用与阻止
  * 利用
    * 拖拽   轮播图   。。。
    * 事件委派
        * 利用事件流
        * 直接事件源   e.target
  * 阻止
    * e.stopPropagation()    现代浏览器
    * e.cancelBubble=true;   IE
    * hover.js   解决事件流的问题

 ## 移动端事件
    * onclick
    * ontouchstart  表示触摸开始  类似于onmousedown
    * ontouchmove   表示触摸移动的效果   类似于 onmousemove
    * ontouchend  表示事件结束  类似于onmouseup
    * 触摸点的集合
        * e.touches  所有触摸点的集合
        * e.targetTouches   当前事件源身上所有触摸点的集合
        * e.changedTouches  当前事件源身上所有正在改变的触摸点的集合
# 日期对象
> 本地对象（在ECMAScript中内置的）
>  所有关于当前日期的信息
## 得到日期对象
    * new Date()  当前时刻的日期对象
    * new Date(年，月，日，时，分，秒)   得到具体某一个时刻的日期对象

# 正则对象
    * 什么是正则表达式
    > 一个用来描述或者匹配一系列符合某个语法规则的字符串的语言。
## 应用场合
> 数据验证   文本替换   内容检索   过滤内容
> 完成字符串无法完成的特殊匹配  替换  拆分等操作
## 创建正则表达式
    * 实例化构造函数
    *  字面量
### 方法
    * test()  判断某一个字符串是否能被当前正则匹配
    * exec()  解析字符串当中被正则匹配到的部分  返回结果到数组当中  如果是全局模式的正则，下一次解析会接着上一次解析的位置继续找，如果找不到，返回null
### 语法
  * 定界符
      * /  正则开始和结束
      * ^  匹配字符串的开始位置
      * $  匹配字符串的结束位置
  * 原子  -正则当中最小的一个单位
      * \s   空格
      * \d   任意一个0到9的数字  [0-9]
      * \D   除了数字之外的任意字符  [^0-9]
      * \S   除了空格意外的任意字符
      * \w   字母  数字  下划线  [a-zA-Z0-9_]
      * \W   除了字母 数字 下划线之外的任意字符  [^a-zA-z0-9_]
  * 原子表
      * []
      * [^]
 * 原子分组
      * () 把一部分原子通过括号包裹成一个整体,还可以在后面调用（反向引用  \+第几个括号）
      * \1 \2 \3  表示当前位置的内容必须和第n个括号的内容一样   反向引用
      * 取消反向引用  在括号开始加 (?:)
 * 量词  -定义个数  必须跟在原子，原子表，原子分组后面
      * \* 匹配0个或多个  {0,}
      * {1，} 1个以上
      * {6,11}  6到11个
      * {6} 6个
      * \+  匹配1个多个  {1,}
      * ?   匹配0个或者一个  {0,1}
 * 正则的贪婪与吝啬  量词后面，一般用在替换，解析
      * 使用量词去匹配的时候 是尽量多的去匹配的
      * 尽量少的匹配 在量词的后面加一个?
 * 元字符  -表示特殊功能的符号
      * \  转义
      * |  或者
      * .  任意一个字符
      * \-  表示范围
 * 模式修正符  -定义匹配模式
      * g  全局的匹配
      * i  不区分大小写
## 字符串方法中的正则
  * replace()
  * match()
  * search()   类似于indexOf 参数是正则
  * split()  字符串转换成数组

# 表单对象
> form  表单控件  input textarea select
> text password radio checkbox file hidden submit reset button
> email url date month year time color number range search
## 获取
~~~javascript
   var form=document.querySelector("form");
   var form1=document.getElementsByName("myform")[0];
   var form2=document.forms[0];
   var form3=document.forms.myform;
   var form4=document.forms["myform"];
   var form5=document.myform;
~~~
~~~javascript
    var input1=document.getElementsByName("zh")[0];
    var input2=form.elements[0];
    var input3=form.elements.zh;
    var input4=form.zh;
~~~
## 方法
  * 表单控件的事件
    * onfocus()  获得焦点
    * onblur()   失去焦点
    * onchange()   内容改变并且失去焦点
    * focus()   自动获得焦点
    * blur()   失去焦点
  * form 对象
    * onsubmit  提交之后触发
    * onreset   表单重置之后触发
    * submit()  提交表单
    * reset()  重置表单
## 属性
  * form  action name method
  * type name value placeholder autofocus pattern maxLength step min max checked selected(下拉) size multiple(多选) rows cols readOnly(只读) disabled required(必须要填写的)
  * option 标签 text 文本内容
  * select 标签 selectedIndex  当前选中的option的索引值
