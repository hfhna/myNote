# angular
  > 核心思想  基于前端的mvc （mvvm）框架  
  > mvvm  用来脏值检测
  * 单页面应用 spa  局部刷新
  * 双向数据绑定
  * 模块化开发
# 使用
  * 引入
  * 初始化  
     * ng-app 
  * $scope  依赖注入  作用域
  * $rootScope  根作用域
  * np-repeat  遍历
  * {{price*count | currency}}将价格转化为价钱的格式
  * {{表达式}}
    * 字符串
    * 数值
    * 可运算
    * 数组
    * 对象
    * 不支持正则，if else
    * 三元表达式
* 指令
  * ng-app  
  * ng-controller  
  * ng-repeat  遍历  ng-repeat="(k,v) in arr"  $index 与 k 指 数组的下标   ；如果数组中有一样的，通过下标遍历  ng-repeat="v in arr track by $index"
  * ng-model   将作用域里面的数据绑定到html中（给表单元素绑定）
  * ng-click   点击事件
  * ng-init  初始化数据
  * ng-bind   与   {{ }}   
  * ng-class  动态添加类名   string array obj
  * ng-show   控制显示
  * ng-hide    隐藏
  * ng-if      通过页面元素的创建来控制元素的显示隐藏
  * ng-style   
# 过滤
  * | 管道符
  * {{price  | currency}}
  * {{price  | currency:'￥'}}
  * {{num   | number:1}}
  * {{str | uppercase}}   转化为大写
  * {{str | lowercase}}  转化为小写
  * {{str | limitTo:2}}  截取2个字符串
  * {{ arr | limitTo:2}}   截取
  * {{ person | json}}  转化为json格式  （对象）
  * {{date | date}}  将时间戳格式化日期
  * {{date | date:'medium'}} 
  * {{date | date:'yy'}} 
  * {{date | date:'yyyy'}} 
  * {{date | date:'MM'}} 
  * {{date | date:'d'}} 
  * {{date | date:'yyyy-MM-d HH:mm:ss Z'}}
  * | filter:'a':true    过滤
  * | orderBy:'age'   根据年龄进行排序
  * | orderBy:'age':true  降序排序
  * | orderBy:'-age'  降序排序
* 自定义指令
  * app.directive('hello',function(){  
        return {  
            // A 属性   E 元素，标签  C 类名   M  注释   严格区分大小写  
            restrict:'E',  //以什么样的方式来显示，调用形式  
            replace:true,   //当restrict 为M 时，必须加上  
            template:'<p>这是自定义指令</p>'  //模板    
            scope:true,  //独立的作用域
            scope:{myId:'@myId'},  // 隔离作用域 不会从父元素获取数据  三种绑定方式 @ = &    @引入字符串 & 引入方法  = 绑定数据
            controller:function($scope){},  
            //link  操作dom元素   scope  作用域  element  元素   attr   属性  
            link:function(scope,element,attr){}
        }  
  })  
  
  * 如果是以注释的形式调用
    *　<!-- directive:hello -->
  * $scope.$watch('要检测的数据',function(newv,oldv){},true)  如果监测的是数组，对象的话，必须要传第三个参数
 * route
   * app.config(function($routeProvider){
        $routeProvider.when('/',{
            template:'<p>这是首页</p>'
        }).when('/new',{
            template:''
        }).otherwise({redirectTo:''})
   })
   
   
# API
  * 主题： http://new
  