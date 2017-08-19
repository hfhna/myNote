# php mysql
  * php mysql 基本语法的掌握
  * php搭建过程的后台框架
  * php搭建mvc模式的框架
  * phpcms
# php 的基础语法
  * php是什么
  * php能干什么用
  * php是怎么运行的
  * php的变量
  * php的数据类型
  * php的运算符
  * php的流程控制
  * php的函数
  * php的数组
  * php的对象
  * 字符串操作的函数
  * 数组操作的函数
  * 数学函数
  * php操作文件
  * php操作图像

1. php 是什么  php:Hypertext  preprocessor;超文本预处理器    应用最广泛的后台语言。可以嵌入到html中执行。
2. php 能够干什么
  * 生成动态的html网页
  * 完成数据的验证
  * 上传文件
  * 操作图像  验证码  水印
  * 。。。
3. php是怎么运行的
  * 网站  前端+后台
    * 前端 html css  js font  img
    * 后台 php+mysql
  * 浏览器  服务器
    1. 在地址栏输入一个地址  http://www.baidu.com
    2. 发送请求  html代码
    3. 浏览器读取html代码
         * script  发送请求  请求一个js文件；
         * 读取到link 发送请求  读取css文件；
         * 读取到 img src 发送请求  读取图片；
         * @import url(1.css);
         * @font-face;
         * background:url();
         * border-image-source:url();
         * ajax
4.  网页呈现到浏览器中
    * 服务器程序  处理这些请求
          * 接收浏览器发送的请求
          * 响应相应的数据
          * 请求如果是  .html  .js  .css  直接把对应的文件返回
          * 如果请求是  .php 服务器就会调用对应的模块解析运行php 然后把处理的结果返回
    * 集成化的服务器开发环境包 wamp
      * w windows
      * a apache
      * m mysql 数据库管理工具
      * p php
      * apache服务器  对于http有完整的支持，其中包含php解析模块，所以我们可以在wamp中运行php不能在本地运行。

# 语法规范和变量
  * 语法规则
    * 注释： 单行注释  多行注释  #注释
    * 开始 <?php
    * 结束 ?>  如果后面还有其它的html代码才写
    ```php
    <?php for($i=0;$i<10;$i++):?>
    <div>111</div>
    <?php endfor;?>
    ```
    * 每一条语句的后面都要加 ;
  * 变量和常量
    * $变量名  以 字母  下划线开始  在后面可以跟 字母 数字 下划线 $
    * 区分大小写
    * 避免使用关键字
  * 可变变量
    ```
    $a="b";
    $$a="1";
    ```
  * 传址
    * $a=&$b;
  * echo() 输出一个字符串
  * isset() 判断某一个变量是否存在
  * var_dump()  输出一个值具体的类型 内容和长度
  * unset()  删除掉某个变量的值
  * empty()  判断某个变量的值是否为空
  * error_reporting(0)  设置错误显示级别
  * 超全局变量
    * 超全局变量  一系列数组 php自带的一组变量  保存的是当前接收的一些信息或者是环境信息
    * $GLOBALS 所有的全局变量
    * $_GET["name"]  保存的是所有用户通过get方式提交的信息
    * $_POST[""]   保存的是所有用户通过post方式提交的信息
    * &_REQUEST[]  保存的是所有用户发送的请求
    * &_SERVER[]   保存的是服务器详细的信息
    * $_ENV[]   保存当前的环境变量信息
    * $_SESSION[]  当前session中保存的信息
    * $_COOKIE[]   当前页面的cookie信息
  * 常量
    * define("AA",1);  全局的
    * const AA=1;  只作用在当前的作用域内
    * defined()  判断某个常量是否是已经定义的
    * 魔术常量
      * \_\_LINE\_\_  行号
      * \_\_FILE\_\_  当前文件路径
      * \_\_DIR\_\_   当前文件夹路径
* 数据类型
  * 四种标量
    * 整数 int
      * 0b 二进制   0 八进制  0x 十六进制数
    * 浮点数 float
    * 字符串 string
      * 字符串的连接 .
      * .=  赋值连接
    * 布尔值 boolean
  * 两种复合类型
    * 数组  array
    * 对象  object
  * 两种特殊类型
    * null
    * 资源  resource
  * gettype()  返回某一个变量的数据类型
  * is_   用类判断某个变量是否为某种数据类型
    * is_int()
    * is_float()
    * is_string()
    * is_bool()
    * is_array()
    * is_object()
    * is_null()
    * is_resource()
  * 数据类型的转换
    * 三种方式
      * (类型) $num;
      ```
      $num=111;
      var_dump($num);
      $num=(float) $num;
      $num=(string) $num;
      $num=(bool) $num;
      ```
      * intval()  floatval() strval() boolval()
      * settype()
      ```
      settype($num,"string");
      ```
  * 函数
    * 如果有形参必须传实参，  除非形参都有默认值
    * 参数可以直接写默认值
    * 全局变量在函数中不能直接访问
    * 通过$GLOBALS 在函数中访问全局变量 也可以直接重新赋值全局变量 创建一个新的全局变量
    * global  可以在函数中使用全局变量
    * static 在内存中长期保存声明的局部变量 重新调用函数不会重新声明
 * 调用对象里的方法 ->
 * 索引数组   以数字为下标的数组
 * 关联数组    下标不在是数字


* apache 关系型数据库  sql mysql 中小型
* 右键我的电脑  管理  服务  wampmysql   wampapache  绿色
* php ->  操作数据库  ->   数据库语言
* Mysqlworkbench   Navica...MYSQL
* 字符集 utf-8(万国码)  存储中文占3 4个字符
   gbk  gb2312  存储中文占2个字符
   常用  utf8_general_cl
* 库 database    表   table    字段
* 命令
  * mysql -hlocalhost -uroot -p  回车
  * show databases    查看所有数据库
  * use 库名
  * show tables
  * select * from 表名
  * 删除  drop database 库名
  * 创建数据库 create database 库名;
  * 添加表  create table 表名(
     id int(10) primary key auto_increment,
     name varchar(20) ,
     sex varchar(10),
     age int(10)) default charset=utf8;
  * 插入信息 insert into stu(name,sex,age) values("张三","男",15);
  * 修改信息 update stu set age=16 where id=1;
  * delete from stu where id=1;
  * select * from stu where sex="nv" order by age;
  * select * from stu limit 0,2;
# 关于连接数据库
  * 默认端口号3306
  * mysql -h地址 -P端口号 -u用户名 -p密码
# 关于创建结构
  * create database 库名;
  * create database if not exists 库名;
  * drop database 库名;
  * create table if not exists 表名(
  字段名  字段的类型(类型的长度) 指定键名 primary key 是否自增 auto_increment，
  字段2名  字段2的类型,
  ...
  )default charset=utf8;
# 查询信息
  * show databases;
  * use 库名;
  * show tables;
  * desc 表名  查询字段
# 数据库数据的操作
  * select 字段名 from 表名;
  * update 表名 set 字段=值 where 字段=值(id=2);
  * insert into 表名(字段1，字段2，...) values(值1，值2,..);
  * delete from 表名 where 字段=值;

# apache 如何解析php代码
  1. 查看文件相应的后缀名  如果后缀名是 .html apache不会解析 ；如果没有后缀名 ，默认执行html文件，如果没有html文件，执行php文件
  2. 如果后缀名是php ，解析包含在<?php?>中的代码
# php 如何去操作数据库
  1. 连接  $db=new mysqli(hostname,username,password,databasename);
      $db->query("set names utf8");
      //结果集
      $result=$db->query("select ...");
      while($row=$result->fetch_assoc()){

      }
# 前端和后台数据的交互方式
  * “get”    通过地址栏传参 通过明文的方式传递数据 不安全   数据量有限  4k
  * “post”   通过加密的方式传递参数  安全  数据量没有限制
  * $_GET
  * $_POST
  * $_REQUEST 无论是get还是post方式提交过来的都可以用
# 单双引号的区别
  * 单引号的运行速度快
  * 双引号可以解析变量
  * 单引号里面的东西都解析为字符串
# iframe 帧窗口技术



# implode(连接符，数组) 将数组连接成字符串
# $_SERVER["PHP_SELF"]
# this
   * 一个对象的属性和方法指向的指针就是this；
   * 一个属性和方法属于哪个对象的，this就会指向谁 ；
#

