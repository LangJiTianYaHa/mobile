# 第三天


## 阻止默认行为
e.preventDefault();

## 输入法
QQ 输入法 剪切板

## 中文状态下使用英文标点
搜狗和 QQ 都可以

## mac clips

## 数据共享的方法
1. 提高变量的作用域.

2. 将数据保存在一个对象中.

## addEventListener 第三个参数
```js
document.documentElement.addEventListener('touchstart', function(e){
    //阻止默认行为
    e.preventDefault();
},{
    passive:false // 被动  被动模式   true  false  控制 e.preventDefault 是否失效
}); 
```

## 默认行为阻止
推荐创建一个最外层的包裹元素, 然后进行事件绑定, 并阻止默认行为

## SEO
search engine optimization  //搜索引擎优化

## 是不是网页看到的内容源代码中一定有呢??
不一定, 很有可能数据是通过 JS 动态创建的, 源代码中不一定存在

## IP  品牌

## 字符码表
汉字
gb2312  gbk

繁体
big5

unicode 

## 获取手指离开元素时的位置
只能使用 changedTouches 属性

## 背单词
desk
boy
computer
cup
mouse
hair
clothes
shoe
mobile
floor
ceil

desk
boy
desk
computer
boy
cup
computer
mouse
cup






