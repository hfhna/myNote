# vue
  * 渐进增强，优雅降级
  * methods 和 computed区别
    * methods 调用加括号，computed不用加括号
    * computed 运行的效率快，只有在和他相关联的值改变时才调用
# svn 版本控制工具(TortoiseSVN)
  * svn add
  * svn commit
# vue 生命周期
  * 创建前，创建后，挂载前，挂载后，对象更新前，更新后，对象销毁前，销毁后，组件激活时调用，组件停用时调用
# webpack
  * export default aa ;  返回默认值；导出模块
# new Vue 最顶层的vue对象
  * vue 涉及到的对象
  * Vue 构造函数
  * component new vue 的子对象  组件对象
  * new Router 主路由对象
  * 每一个路由的对象
  ```
  router.beforeEach(function(to,from,next){
    if(to.meta.login){

    }else{
        next();
    }
  })
  ```
