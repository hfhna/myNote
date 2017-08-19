## wamp
  * w   windows 操作系统
  * a   apache 服务器
  * m    mysql  数据库操作软件
  * p    php
# ajax
## ajax的用途
  * ajax  名词，不是缩写
    * Asynchronous 异步
    * JavaScript js
    * and  和
    * XML 可扩展标记语言  用于数据的传输
      * <user>
           <username>123</username>
           <password>345</password>
        </user>
    * json
      * {username:123,password:123};
    * 实现前台和后台的数据交互的一种技术
      * 用javascript去获取数据用dom的方法操作文档的内容 通过xhr对象完成数据的发送  xml/json/txt/html/md    字符串 是数据发送时的一种格式。
    * 传统的前台后台交互模式
      * form表单实现交互
      * 前台提交数据 --》 后台接收数据处理返回数据--》  html页面
    * 通过ajax实现数据交互
      * 网页不用刷新
      * 所有的发送接收操作都通过XMLHttpRequest对象来完成
      * 操作dom
* ajax 是在页面不刷新的前提下，实现前台和后台的数据交互的一种技术
      王琦老师：18735108906


# xhr对象的操作
  1. new XMLHttpRequest()   IE6  new ActionXObject("Microsoft.XMLHTTP")
  2. xhr.open()  配置请求  第一个参数是发送方式  get post  第二个参数是发送地址 (如果是get形式发送的 发送的内容要连接到地址的后面)  第三个参数 是否是异步
  3. 发送请求  xhr.send()  如果请求是post形式的 把要发送的数据放到send的参数里面；
  4. 监测响应的完成  接收响应
    * onreadystatechange  readyState  status
    * onload
    * responseText  以文本的方式接受响应的内容
    * responseXML   以XML的格式接收响应的内容
    * responseType=""  指定要接收的格式 text json document arraybuffer buffer
    * response  只表示接收内容
  * 注意：如果请求是post形式的，添加配置
  xhr.setRequestHeader("Content-Type","application/x-www-form-urlencoded");
## 异步的
  * 同步  按照顺序依次执行
  * 异步  同时去处理多个问题
## get post
  * get 把数据连接到地址栏的后面发送 传输数据量比较小，速度比较快，安全性较低
  * post  把数据插入到请求头信息里面去发送  数据量比较大  速度相对慢 安全性相对较高

## json jsonp
  * json 是一种数据的结构写法 用于前后台数据交互的一种数据格式
  * jsonp json with padding(包裹) 是一种前后台数据交互的一种方式
  * jsonp 解决跨域问题
  * ajax 同源策略 只能请求位于同一个域名下的文件  协议 主机名 端口号 必须一致才是同源
    * http://www.xxx.com
    * https://www.xxx.com
    * http://www.xxx.com:80/
    * http://www.aa.xxx.com
    * http://www.xxx.com/aa/bb.html   正确
  * 通过script标签去加载资源的时候是没有跨域问题的