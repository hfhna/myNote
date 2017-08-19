# canvas

  * 获取绘制对象
    * canvas.getContext("2d");
  * 绘制形状  矩形
    * fillRect()  绘制一个填充矩形
    * strokeRect()  绘制一个描边矩形
    * clearRect()   清空一个矩形区域
    * x,y,width,height
  * canvas的坐标系
    * 默认左上角  0  0  向右x轴增加  向下y轴增加

  * 样式的设置
    * fillStyle="";   颜色名   十六进制   rgb() rgba()
    * strokeStyle="";
    * lineWidth=5;  设置线条的宽度
    * lineJoin="round"   设置线条连接处的样式  bevel 平角 round 圆角  miter(默认) 尖角
    * miterLimit=5;     设置尖角的最大长度  超出会变成平角
    * lineCap="round"   设置线条末端的样式  square   round  butt（默认）
    * 虚线
      * getLineDash()  得到一个数组
      * setLineDash([4,2])
      * LineDashOffset()
    * 全局的透明度
      * globalAlpha
    * 渐变
      * 线性渐变
        * linear=cobj.createLinearGradient(x,y,x1,y1);
        * linear.addColorStop(pos,color);
        * cobj.fullStyle=linear;
      * 径向渐变
        * radial=cobj.createRadialGradient(x,y,r,x1,y1,r1);
        * radial.addColorStop(pos,color);
        * cobj.fullStyle=radial;
  * 路径
    * beginPath()  开启新的路径  (把旧的路径列表清空)
    * moveTo(x,y)  从哪个位置开始
    * lineTo(x,y)  画到哪个位置
    * closePath()  闭合路径
    * fill()  把路径闭合形成的区域填充满
    * stroke()   把路径描边
    * arc(x,y,radius,startAngle,endAngle,boolean)  绘制圆弧路径  坐标 半径 起始角度 结束角度 顺时针绘制还是逆时针绘制  默认是顺时针 false
    * quadraticCurveTo(cx,xy,x,y)  cx cy 控制点的坐标 x y 弧线结束位置的坐标   绘制弧线
    * rect(x,y,width,height)  快速绘制一个矩形路径的方法
  * 保存和载入
    * save()   保存画布所有的设置的状态  lineWidth strokeStyle setLineDash()
    * restore()  恢复到对应的save的位置的状态
  * 文字
    * fillText(text,x,y);
    * strokeText(text,x,y);
    * font "文字的大小和字体"
    * textAlign    center
    * textBaseline   middle
  * 坐标系移动
    * translate(x,y)
    * rotate(rad)
    * scale(x,y)
    * transform()
  * 画布数据
    * getImageData()  获取画布指定区域当中所有的图像数据
    * putImageData()  将某个图像数据放置到画布指定的位置上