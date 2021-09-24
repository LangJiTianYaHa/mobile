# 第五天

## vw  vh
这是两个长度单位, 1vw = 1% 的设备独立像素总宽, 1vh = 1% 的设备独立像素总高

iphone 6   375   667
div{
    width: 10vw;
    height: 20vh;
}

div 的宽度等于 37.5px, 高度等于 133.4

## 最后加单位
设置行内样式的时候, 在最后的位置加单位最方便

## classList 
classList 是元素对象的一个属性, 用来操作元素的 class 类

* add 增加类名
* remove 移除类名
* contains 是否包含指定的类名

## 图片加载对元素高度的影响
图片的加载需要时间, 如果在图片加载完毕之前,获取元素的高度, 可能获取不到真实的想要的结果. 保险的做法是在事件(onload)中获取 

## 结果情况固定的场景
想到 取余，switch...case

## 感知痛点

## getComputedStyle
是一个函数, 用来获取元素计算后的样式
get         获取
computed    计算后的
style       样式

## 强制类型转换为 false 的情况
0  NaN  ''  null  undefined  false  0.0

boolean  string  number  undefined  null object

usonb 

undefined  ''  null  0   0.0  NaN  false

## 关于省略花括号
如果 if else 语句后只有一条语句, 则花括号可以省略

## webstorm 左侧的工作目录路径不要太深

## classList
* add
* remove
* contains
* toggle 类名的切换有无

## 水平撑开元素
父级元素定位
position:absolute;
white-space:nowrap
font-size: 0;

子元素
display:inline-block;

## 贝塞尔曲线
贝塞尔曲线 https://cubic-bezier.com/

1. 水平方向代表的是时间 t
2. 垂直方向代表的是进度 s (位移) 
3. 切线与 X 轴形成的夹角代表速度, 夹角越大速度越快, 反之速度越小
4. 想越界, 则将曲线拉至最上线区域外.

## 一提到自动
想到 定时器, 过渡, 动画

## gt  lt
greater than

less than

## 属性操作
* getAttribute 获取属性
* setAttribute 设置属性
* removeAttribute 移除属性

## 获取元素在同辈元素中的索引
1 在标签中增加索引标记
```
<div index="2"></div>
<div data-index="3"></div>
```
2 遍历元素增加属性
```js
navItems.forEach(function(item, key){
    //将下标存入到元素对象中
    item.key = key;
    item.addEventListener('touchstart', function(){
        //获取下标
        console.log(this.key);
    });
});
```

## url
http://tingapi.ting.baidu.com/v1/restserver/ting?method=baidu.ting.billboard.billList&type=2&size=10&offset=0#abc

http 协议
tingapi.ting.baidu.com  域名
/v1/restserver/ting 路径
method=baidu.ting.billboard.billList  查询字符串
#abc 锚点



##  setInterval 
函数的返回结果是 数字

## 服务使用
1. 启动命令行  点击左下角的 Terminal (终端)
2. 切换文件夹目录至 server 文件夹 (cd )
3. 启动服务  
```js
node app.js
```

## left 与 translateX 的差异

![timeline-frames-macbook1](assets/timeline-frames-macbook1.png)

​    左上方的图片是通过改变元素top/left进行动画的帧率，而右上方则是调用translate函数的帧率。我们可以明显看出左图的每一帧都执行了相对较长时间的paint，在每一帧内，cpu都需要计算该元素的其他样式，特别是相对需要复杂计算的盒阴影，渐变，圆角等样式，最后都需要将这些样式应用到该元素内。从这个角度看，如果对于较为老旧的移动设备进行相对复杂的动画，那么效果肯定不理想。

​    而通过调用 translate，会启动硬件加速，即在 GPU 层对该元素进行渲染。这样，CPU 就会相对解放出来进行其他的计算，GPU 对样式的计算相对较快，且保证较大的帧率。我们可以通过 2d 和 3d 的 transform 来启用 GPU 计算。





