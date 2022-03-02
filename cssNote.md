# 如何学习
1. 什么是CSS
2. 怎么用
3. CSS 选择器 （重难点）
4. 美化网页 （文字，阴影，超链接，列表， 渐变。。）
5. 盒子模型
6. 浮动
7. 定位
8. 网页动画 （特效效果）

菜鸟教程 CSS3

## 1.1  什么是CSS
Cascading Style Sheet 层叠级联样式表

CSS: 表现 （美化网页）
字体，颜色，边距，高度，背景图片，网页定位， 网页浮动

## 1.2 CSS 发展史
1.0： 
2.0 ： DIV (块) +CSS, HTML与CSS 结构分离思想， 网页变得简单， SEO
2.1 浮动，定位
3.0 圆角边框，阴影，动画。。。浏览器兼容性~

## 1.3 快速入门

css 优势：
1. 内容和表现分离 
2. 网页结构表现同意，可以实现复用
3. 样式丰富
4. 建议使用独立于HTML 的CSS 文件
5. 利用SEO, 容易被搜索引擎收录

## 1.4 CSS 的三种导入方式
内部，外部，行内

拓展： 外部样式两种写法
* 链接式
```
<link rel="stylesheet" href="css/style.css">
```
* 导入式
```
    <style>
        @import url("css/style.css");
    </style>
```

import是CSS 2.1特有的

# 选择器
作用： 选择页面上的某一个或者某一类元素

## 2.1 基本选择器
1. 标签选择器: 选择一类标签 标签{}
2. 类选择器 class： 选择所有class属性一致的标签，跨标签，类名 .类名{}
3. ID 选择器： 全局唯一！#id名{}

优先级： id > class > 标签

4. 层次选择器
* 后代选择器
在某个元素的后面
祖爷爷，爷爷，爸爸，你

```
        /*后代选择器*/
        body p{
            background: red;
        }

        /*子选择器*/
        body>p{
            background: green;
        }
        /*相邻兄弟选择器,对下不对上，只有一个*/
        .active+p{
            background: pink;
        }
        /*通用兄弟选择器，当前选中元素的向下的所有兄弟元素*/
        .active~p{
            background: plum;
        }
```

5. 结构伪类选择器
伪类：条件
有特效
有冒号的就是伪类
```
        /*ul的第一个元素*/
        ul li:first-child{
            background:palevioletred;
        }
        /*ul的最后元素*/
        ul li:last-child{
            background: greenyellow;
        }
        /*选中p1: 定位到父元素，选择当前的第一个元素
        选择当前p元素的父级元素，选中父级元素的第一个，并且是当前元素才生效！*/
        p:nth-child(1){
            background: blueviolet;
        }

        p:nth-of-type(1){
            background: yellow;
        }
```
