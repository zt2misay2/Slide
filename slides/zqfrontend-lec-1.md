---
title: 前端部第一次组会
separator: <!-- s -->
verticalSeparator: <!-- v -->
theme: simple
highlightTheme: monokai-sublime
css:
    - custom.css
    - dark.css
revealOptions:
    transition: 'slide'
    transitionSpeed: fast
    center: false
    slideNumber: "c/t"
    width: 1000
---

<style>
@import url('https://cdn.jsdelivr.net/npm/lxgw-wenkai-webfont@1.1.0/style.css');
.reveal .slides *:not(.katex):not(.katex *):not(mjx-container):not(mjx-container *) {
font-family: 'LXGW WenKai', sans-serif !important;
}

.button-container {
display: flex;
align-items: center;
justify-content: center;
gap: 20px;
position: relative;
width: 100%; 
}

.button {
display: flex;
align-items: center;
justify-content: center;  
text-decoration: none;
border: 1px solid #ddd;
padding: 0; 
border-radius: 50%;  
width: 85px; 
height: 85px; 
transition: transform 0.3s ease, border-color 0.3s ease;  
cursor: pointer;
overflow: hidden;
}

.button img {
width: 100%;  
height: 100%;  
object-fit: cover;  
border-radius: 50%;  
}

.button:hover {
transform: scale(1.1);
border-color: rgba(0, 123, 255, 0.2);
box-shadow: 0 2px 10px rgba(0, 123, 255, 0.2); 
}

.button-container .button-text {
position: absolute; 
top: 50%;
left: 100%;  
transform: translateY(-50%); 
opacity: 0;  
visibility: hidden;  
transition: opacity 0.3s ease, visibility 0.3s ease;
white-space: nowrap; 
font-size: 20px;
}
</style>

<!-- .slide: data-background="crypto-lec1/background.webp" -->



<br>
<br>
<br>

<center><h5 style="font-size: 55px; text-align: center;">前端部第一次组会</h5></center>
<br>
<center><h1 style="font-size: 30px; text-align: center;">2025.10.12</h1></center>
<br>
<center><div class="button-container" >
</button>
</div></center>

<!-- s -->
<!-- .slide: data-background="Crypto/background.webp" -->

<br>
<br>
<br>
<br>
<br>

<center><h5 style="font-size: 55px; text-align: center;">欢迎来到自强Studio前端部</h5></center>


<!-- s -->
<!-- .slide: data-background="Crypto/background.webp" -->

## 本次组会的环节

- 自我介绍
- 前端部简介
- 基础三件套知识以及框架
- 前端&计算机技术学习常见经验

<div class="fragment" style="margin-top: 40px">

- 本次组会大约50min左右

</div>

<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->

<br>
<br>
<br>
<br>
<br>

<center><h5 style="font-size: 55px; text-align: center;">自我介绍环节</h5></center>


<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->

<br>
<br>
<br>
<br>
<br>

<center><h5 style="font-size: 55px; text-align: center;">关于前端部</h5></center>

<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->

## 我们今年的安排

<div class="fragment" style="margin-top: 40px">

- 组会，每月一次，内容安排如下
	- 10月 前端基本概念以及学习方法 Vibe Coding 相关 基本时间线安排
	- 11月 Vue等现代框架 如何借助AI IDE上手看现成项目代码 
	- 12月 基本开发规范 寒假新人项目规划 部分竞赛推荐
	- 3月/4月 新人项目跟进/验收 
	- 5月 换届
</div>

<!-- s -->
<!-- .slide: data-background="Crypto/background.webp" -->

## 我们希望在前端部带给你的

<div class="fragment" style="margin-top: 40px">

- 对前端技术的基本了解
- 进行一次较为规范的前端开发
- 有一个能写上简历的前端项目经历
- 利用前端部的经验参加一些竞赛 为个人简历增加内容

</div>

<!-- s -->
<!-- .slide: data-background="Crypto/background.webp" -->

<br>
<br>
<br>
<br>
<br>

<center><h5 style="font-size: 55px; text-align: center;">基础前端知识</h5></center>
<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->

## 什么是前端？

<div class="fragment" style="margin-top: 40px">

一切我们使用的联网应用 都基于Web页面的架构

</div>


<div class="fragment" style="margin-top: 40px">

一切的应用 都离不开交互
- 浏览的网页
- 手机程序
- 甚至游戏的界面 

</div>

<div class="fragment" style="margin-top: 40px">

合理显示程序的信息 从用户获取交互 进行传输
- 把数据和逻辑转化为用户可交互页面的工程，就是前端

</div>
<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->

我们需要了解哪些呢

<div class="fragment" style="margin-top: 40px">

作为Web网页基本的构成元素，首先是最基础的

- 三件套
	- HTML
	- CSS
	- JavaScript

</div>

<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->

### HTML

网页的基本"骨架"

<div class="fragment" style="margin-top: 40px">

#### 1. 常用标签

* 结构：`<html>`、`<head>`、`<body>`
* 语义：`<header>` `<nav>` `<main>` `<section>` `<article>` `<aside>` `<footer>`
* 文本：`<h1~h6>` `<p>` `<span>` `<strong>` `<em>` `<blockquote>` `<code>`
* 列表与表格：`<ul>` `<ol>` `<li>` / `<table>` `<thead>` `<tbody>` `<tr>` `<th>` `<td>`
* 媒体：`<img>` `<audio>` `<video>`（含 `controls`、`autoplay`、`muted`）
* 表单：`<form>` `<input>` `<label>` `<button>` `<select>` `<textarea>`（注意 `name`、`id/for` 关联）

</div>

<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->

### HTML

<div class="fragment" style="margin-top: 40px">

#### 2. HTML5 标准语法

* 文档类型：`<!doctype html>`（区分标准/怪异模式）
* 标签闭合、嵌套规范；属性无需引号时也建议加引号
* 元数据：`<meta charset="utf-8">`、`<meta name="viewport" content="width=device-width, initial-scale=1">`
* 自闭合：`<img />` `<input />`（HTML 允许省略 `/`，但统一风格更可读）
* 合法属性：布尔属性如 `disabled`/`checked` 仅书写名即可

</div>

<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->

### CSS
网页的“外貌描摹”

<div class="fragment" style="margin-top: 40px">

#### 1. 常用属性

* 盒模型：`box-sizing`、`margin`、`border`、`padding`、`width/height`
* 文本与字体：`font`、`line-height`、`text-align`、`white-space`、`text-overflow`
* 颜色与背景：`color`、`background`（含渐变） 、`opacity`
* 定位：`position`（static/relative/absolute/fixed/sticky）+ `top/right/bottom/left` + `z-index`
* 显示与溢出：`display`、`overflow`、`visibility`
* 变换与过渡：`transform`、`transition`

</div>

<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->

### CSS

<div class="fragment" style="margin-top: 40px">

#### 2. 常用容器：Flex / Grid

* Flex（主轴/交叉轴、对齐）：

  ```css
  .row { display: flex; gap: 8px; align-items: center; justify-content: space-between; }
  ```
* Grid（二维布局、轨道与区域）：

  ```css
  .grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
  }
  ```

</div>


<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->

### CSS

<div class="fragment" style="margin-top: 40px">

#### 3. 动画效果

* 过渡：

  ```css
  .btn { transition: all .2s ease; }
  .btn:hover { transform: translateY(-2px); }
  ```
* 关键帧：

  ```css
  @keyframes float { from { transform: translateY(0); } to { transform: translateY(-8px); } }
  .badge { animation: float 1s ease-in-out infinite alternate; }
  ```

</div>

<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->

### CSS

<div class="fragment" style="margin-top: 40px">

#### 4. 选择器、伪类、伪元素

* 选择器：元素、类、id、子代 `>`、兄弟 `+ ~`、属性选择器 `[data-x]`
* 伪类：`:hover` `:focus` `:active` `:disabled` `:nth-child()` `:not()`
* 伪元素：`::before` `::after`（常配合 `content` 实现装饰）
* 特殊性（Specificity）与层叠：`!important` 慎用，优先结构化命名与组件化

</div>


<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->

### JavaScript
处理用户交互导致的数据变化 进行前后端的数据传递

<div class="fragment" style="margin-top: 40px">

### 1. 基础语法

* 变量与作用域：`let`/`const`（块级作用域）优先，少用 `var`
* 模块：`import/export`（ES Modules）
* 解构与扩展：

  ```js
  const {a, ...rest} = obj; const list2 = [...list, 42];
  ```

</div>

<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->

### JavaScript

<div class="fragment" style="margin-top: 40px">

##### ES6 基础语法
* 箭头函数、模板字符串、默认参数、`Map/Set`、`class`、`Promise`
<br>
<br>

##### 对象、原型链
* `__proto__` / `Object.getPrototypeOf()`；方法查找自原型链向上
* `class` 语法糖本质仍基于原型
<br>
<br>

##### 函数式编程
* 纯函数、不可变数据、`map/filter/reduce`、组合（compose/pipe）思维
<br>
<br>

</div>

<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->


<div class="fragment" style="margin-top: 40px">

不必抱有畏惧情绪 直接找个题目/Demo上手看 不会就用AI IDE来看，搞清楚大致每个部分有什么用 不必掌握所有语法 

</div>

<!-- s -->
<!-- .slide: data-background="Crypto/background.webp" -->

## 关于AI&AI IDE

- Cursor
- ClaudeCode
- Trae



<!-- v -->
<!-- .slide: data-background="Crypto/background.webp" -->

## 其余可能有用的

- 如何阅读文档？
- 如何提问？
- 报错怎么看 如何根据AI&搜索引擎解决我们遇到的问题？


<!-- s -->
<!-- .slide: data-background="Crypto/background.webp" -->

<br>
<br>
<br>
<br>
<br>

<center><h5 style="font-size: 55px; text-align: center;">Q&A</h5></center>

<!-- s -->
<!-- .slide: data-background="Crypto/background.webp" -->

<br>
<br>
<br>
<br>
<br>

<center><h5 style="font-size: 55px; text-align: center;">感谢参与本次组会 辛苦啦！</h5></center>