# ajax
  * async 异步 正常线程的代码执行完毕（空闲下来的时候，再去执行的代码）
  * javascript 一切需要耗费时间，或者不确定执行的代码都是异步的，比如setTimeout、事件，其他情况都是同步（一条一条去执行） 单线程 异步机制的语言
  * and
  * xml  标签语言的鼻祖
  * 进程  再开辟一条河流
  * 线程  在河流的基础上开辟岔口
  * ajax 通过javascript异步的特性去获取数据，完成单页面的处理，劣势是等待。
  * b/s browser 浏览器 sevices 服务器   数据的传递、交互，不断的发起http请求  单线程
  * c/s 客户端 / 服务器
# json_encode()
# JSON.parse()
# inset_id;
# delegate
# ajax 利用javascript异步机制，来和数据进行交互 。页面不刷新可以对数据来进行操作
   * 单页面的应用
   * 涉及到复杂数据操作，多次的增删改查
   * 劣势
      * 对搜索引擎（百度）不太友好
      * 不能够应对大批量的页面的载入，造成内存无法回首
   * 好处
      * 可以给用户的体验不造成中断，提供连续流畅的用户体验

# $(function(){})
  * document.addEventListener("DOMContentLoaded",function(){})
  * 所有的标签加载完成
  * window.onload  所有的标签以及内容都加载完成
# $(function(){}) 与window.onload的区别
   1. $(function(){})不会被覆盖，而window.onload会被覆盖
   2.  $(function(){})在window.onload执行前执行的，$(function(){})类似于原生js中的DOMContentLoaded事件，在DOM加载完毕后，页面全部内容（如图片等）完全加载完毕前被执行。而window.onload会在页面资源全部加载完毕后才会执行。
# DOM文档加载步骤：
1. 解析HTML结构
2. 加载外部的脚本和样式文件
3. 解析并执行脚本代码
4. 执行$(function(){})内对应代码
5. 加载图片等二进制资源
6. 页面加载完毕，执行window.onload
# jquery 队列
  * 内部自运行的队列 animate
  * fx队列
  * 自定义
