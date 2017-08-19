# node.js
  * 语言和功能已经准备好，php是环境已经准备好的。
  * node.exe 放到全局变量 path下面
  * amd  async module define  异步模块加载的定义方式 ，应用在前端的页面当中，都是通过网络从服务器加载的
    * 引入js文件，会出现的问题；
      * 依赖不清晰  
      * 导致阻塞   引入时加一个属性 async=‘true’，防止阻塞
    * require.js 解决依赖和阻塞。
      * 依赖的文件怎么去写
        ```javascript
        require([],function(a){
            
        })
        ```
      * 被依赖的文件，也就是模块怎么写
        * define({})
        ```javascript
        define([],function(a){
            return {
        
            }
        })
        ```
  * cmd  common module define
  > 正常的模块（文件）加载的方式，服务器的代码->访问的是自己硬盘上的文件  
* nodejs  服务器语言
  > nodejs 操作文件，数据，流，网络
  * require("./demo1")  nodejs依赖或者引入另外一个文件的方式 cmd模块引入的方式，就近原则
    * 遵循cmd 正常的文件引入的方式，按照顺序来的，单线程的
    * 如果要引入(非node_modules里面的)文件必须要加路径（相对路径，绝对路径）
      * __dirname+"demo1" 绝对路径  
        __dirname 当前的根目录
      * var path=require("path")  
        var url=path.resolve(__dirname,"demo1")  组合路径
    * 后缀名可以省略  .js  .json（符合json格式）  .node（编译过的c++文件）
    * 如果说不加路径，其实他要从默认的目录（node_modules）里面去找响应的文件或者是文件夹（index.js）
      * 模块共用的思想 node_modules　　
      * 最好别这么用　　加载模块
    * nodejs 依赖模块（文件），依赖包（文件夹）
    * 3种包，第一种核心包  node.exe ；第二种是第三方的包，npm官方网站，npm install 包名@版本号；第三种是自己写的包
    * npm install 导入安装一些模块
      * 就远原则，首先看根目录下有没有node_modules这个文件，如果没有，一级一级往下找。
      * 全局安装  全局的path变量
        * npm install ejs -g windows c://user/admina../rodata/npm/mode_modules
        * npm install ejs --global
      * npm install ejs --save  依赖于ejs包 系统依赖
      * npm install ejs --save-dev 用户依赖
    * npm init  -> name:
    * npm addUser
    * npm login
    * npm config set registry="http://registry.npmjs.org"
    * cd http
    * npm publish   上传，共享，都能用
    * npm link   上传 ，只本地能用
# webpack  Koa  vue.js  EJS
# http content-type 对照表   浏览器识别的文件格式
# nodejs 包
  * 服务器   实现http协议的细节
    * http协议  应用层
      * 发起http请求 html js img css a form ajax
      * http包含四部分
        * 通用头
          * 请求头和响应头通用的信息 
        * 请求头
        * 响应头
          * 返回数据的类型  mime
          * 返回数据的编码格式  utf-8
          * 默认的首页
          * 如何来进行缓存
            * if-modified-since
          * 如何来进行压缩
          * 如何来设置cookie
        * 响应体
    * TCP/IP协议
  * path 对本地的路径进行处理
  * url 对服务器的路径进行处理
  * query 对查询字符串进行处理
  * 
  ```javascript
  var child=require("child_process");
   child.exec("mkdir -p abc/a/b");
   child.exec("open http://www.baidu.com");
  ````
  * 单线程  节省cpu的资源
  * 异步  用单线程去模拟多线程的效果；正常线程走完了，空闲的时候再执行
  * buffer
    * 储存定长的较长的数据；
  * 四种数据流
    * 可读流 
      * 提供源头，读取数据
    * 可写流
    * 双向流
    * 变换流
    * pipe() 对于数据的流控制  所有可读流对象的方法
# web服务器
  > 接收用户的http请求,响应请求
  * cookie http协议的一种规范
  * windows 检查端口命令  netstat ano | findstr '8888'
  * linux 检查端口  lsof -p | grep '8888'
  * package.json 加bin配置，自定义命令
    * "bin":{
        "start":"./http.js"
    }
    * 在http.js中加#!/usr/bin/nov node
# nodejs系统命令制作的方式
  1. 提供第三方安装包，供别人去使用  
    a. package.json in行设置  
    ```
    "bin":{
        "start1":"./http.js"
    }
    ```  
    b. 需要在操作的文件顶部，指定要执行的程序  
    ```
    #!/usr/bin/env node
    ```  
    c.发布到npm官网  
    ```
    npm publish
    ```  
    d.npm install 包名 -g
    f.用bin指定命令在控制台执行
  2. 在本地运行指定的命令  
    a. 前两步同上  
    b. 运行 npm link 命令  
    c. 运行bin指定的命令  
  3. 需要依赖npm run xx命令 执行相应的程序  
    a. 在运行的目录下面，创建package.json  
    b. 配置script选项  
    ```
    "script":{
        "abc":"node /node_modules/nn-static-server/http.js"
    }
    ```     
    
# nodejs
  * 没有全局变量
  * 每一个文件都有一个顶层对象module
# babel 编译器
  * npm install --save-dev babel-preset-es2015
# promise 防止回调地狱
  ```
  var obj=new Promise(function(reslove,reject){//参数1 执行成功  2执行失败
    
  }).then(function(){},function(){})
  ```
# ajax 
```
fetch().then().then()
```
# cheerio  将字符串变为对象 （jquery）
# 
# 跨域 
> 同源策略  同一个域名的地址，浏览器限制通过ajax去访问 其他域名的内容
  * jsonp
    * <script src=""></script> script 是可以获取不同域的内容
    * 它会把取回来的内容当作js代码去执行
  * jsop 缺陷
    * 获取到baidu的东西 ，客户端和服务器我们自己都能控制  或者 百度 提供了一个接口
    * 提供了接口  百度 接口  百度地图
  * 代理   跨域并且没有制定的接口
    * 代理  可以解决一切跨域的问题
# 
```
var link=[];
var arr=[];
async.series([
//1.要获取表的连接
function (next){
    request("http://tech.ifeng.com/listpage/803/1/list.shtml",function(err,head,body){
        var $=cheerio.load(body);
        $(".zheng list .t_css").each(function(index,obj){
            var obj1={};
            obj1.url=$(obj).attr('href');
            obj1.title=$(obj).html();
            links.push(obj1);
        })
        next();
    })
},
//2.根据连接依次串行的去获取所对性的内容
function(next){ 
    var i=0;
    async.eachSeries(links,function(item,next1){
        request(item.url,function(err,head,body){
            var $=cheerio.load(body);
            var arr1=[];
            arr1.push(item.title);
            arr1.push($("#main-content"));
            arr1.push()//cid;
            arr.push(arr1);
            i++;
        })
        next1();
    })
    if(i==item.length){
        next();
    }
}
],function(){
    
})
```
# buffer
  * 劣势
    * var buffer=Buffer.alloc(70000)
    根据数据来确定buffer的长度

# angular vue
  * angular 更注重双向数据绑定
  * vue  注重组件化
# node  核心包
  * http
  * path
  * url
  * 流
  * process 进程
  * 压缩
  * 加密
* package.json
  * main  入口文件
  * bin
  * 依赖包
  * scripts