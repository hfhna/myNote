# less
## 使用
  * 在客户端通过less.js 对于 .less 文件进行编译
  > 不推荐 占用浏览器的资源
  * 在本地直接把less文件编译成css文件
    * 安装nodejs
    * npm 包管理器（下载工具）npm -v
    * npm install -g less
    * lessc -v
    * 利用 webstorme 完成对于less文件的监视及编译

## 引入
  * @import xxx.less;
## 变量
  * @color:red
  * @aa:color;  @@aa @color
## 嵌套
  * .box{.one{}}  =====> .box .one{}
  * .box{&:hover{}}  ====> .box:hover{}
  * .box{#-aa{}}   ====> .box-aa{}
  * .box{.aa{.bb{}}}  ====> .box .aa .bb{}
## 混合（函数）
  > 在一个类当中去调用另一个类
  * .box{width:100px}  .container{.box;}
  > .box{width:100px}  .container{width:100px}
  * .box(@width:100,@height:100){width:@width+px;height:@height+px;}
     * .container{box(100,100);}
     > .container{width:100px;height:100px;}
     * .container{box();}
     > .container{width:100px;height:100px;}
     * .container{box(200);}
     > .container{width:200px;height:100px;}
     * .container{box(@height:200);}
     > .container{width:100px;height:200px;}
  * 模式匹配
  * 导引表达式
