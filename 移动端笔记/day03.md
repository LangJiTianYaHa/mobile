# 第四天

## 蓝湖
蓝湖是一个生态, 团队开发, 设计稿在线预览与标注

### 使用步骤
1. 注册账号
2. 下载插件 双击下一步
3. 打开 PS 并打开 PSD 文件
4. PS -> 窗口 -> 扩展功能 -> 蓝湖

## 联系方式
17611466036 

## viewport 适配
1. 设置 viewport width 等于设计稿的宽度即可
2. 量取元素的尺寸, 量出来是多少, 就写多少. 比如元素宽度 100 像素, 则css 样式为 width : 100px

## rem 适配与 less 的结合
1. 创建 less 文件并引入. 声明一个变量
```js
@font-size: 设计稿的宽度 / 10rem;
```
* 上边的 rem 的作用是为了进行字符串的拼接, 并无其他特殊意义

2. 设置元素的 CSS 样式
```css
#box{
    width:200px;
    height: 100px;
}
```
进行转换
```css
#box{
    width: 200/@font-size;
    height: 100/@font-size;
}
```

3. 增加 JS 的适配
```js
document.documentElement.style.fontSize = document.documentElement.clientWidth / 10 + 'px';

window.onresize = function () {
    document.documentElement.style.fontSize = document.documentElement.clientWidth / 10 + 'px';
}
```

## 适配的两种思路
1. 定值
375  100   =>  414  ?(110.4)

2. 定比例 + less

## 在线绘图工具
https://www.draw.io/
https://www.processon.com

## 正则简单复习
### 声明
* new RegExp
* / /

### 普通字符
任意字符  数字 字母  符号  中文

### 转义字符
* \w 一个字母数字下划线
* \d 一个数字  
* \s 一个空白字符
* \t 一个水平制表符
* \W  \D  \S 

### 元字符
+
*
{}
?
[]
$
^
()

### 模式修正符
i 
g

### 方法
* test
* exec
* replace 

