---
title: 前端部第二次组会
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

<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->



<br>
<br>
<br>

<center><h5 style="font-size: 55px; text-align: center;">前端部第二次组会</h5></center>
<br>
<center><h1 style="font-size: 30px; text-align: center;">2025.11.6</h1></center>
<br>
<center><div class="button-container" >
</button>
</div></center>

<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## 本次组会的环节

- Vue概论
- 基于Vue的Uniapp项目开发概论
- 基于AI-IDE的看项目实战

---
<div class="fragment" style="margin-top: 40px">

大约45分钟左右

</div>


<!-- v -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## Vue概论

<div class="fragment" style="margin-top: 40px">

什么是Vue?

</div>

<div class="fragment" style="margin-top: 40px">

为什么要用Vue?

</div>

<div class="fragment" style="margin-top: 40px">

在我们原生Js/JQuery写法中

- 手动 document.querySelector、addEventListener、拼 HTML 字符串
- 状态改变 → 手动更新 DOM，逻辑混乱

</div>

<div class="fragment" style="margin-top: 40px">

而Vue能做到

- 数据驱动视图（MVVM）：只管改数据，DOM 交给框架
- 声明式渲染：{{ }} 模板语法、v-if/v-for 控制视图
- 组件化：一个功能、一块 UI，包装成一个组件重复使用

</div>

<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## Vue概论

<div class="fragment" style="margin-top: 40px">

可以认为Vue是Js的一个”脚手架“ 我们只用占在不同的地方递工具，比如 组件 模块 生命周期，而不必管哪些DOM在底层是怎么被渲染的

</div>

<div class="fragment" style="margin-top: 40px">

一般来说 我们的.vue文件可以看作一个.html文件，我们可以自然的在其中编辑html css js代码

</div>

<div class="fragment" style="margin-top: 40px">

它的一大特点是我们可以直接根据已有的vue代码注册一个组件 在我们的父页面直接使用 这大大提高了开发效率

</div>

<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## Vue概论

- 为什么需要Vue?

<div class="fragment" style="margin-top: 40px">

- 项目一复杂，手动维护 DOM 成本极高
- 组件化提高复用、可维护性
- 有完整生态：路由、状态管理、构建工具、插件等
- Uniapp、小程序这类多端框架，底层都倾向于用类似 Vue 的思路

</div>

<!-- v -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## Uniapp概论

Uniapp是什么？

<div class="fragment" style="margin-top: 40px">

- 一个基于 Vue 语法的多端框架
	- 项目中使用Vue 可以在H5 微信小程序 APP中进行运行
	- 写起来像 Vue，编译时转换成不同平台的代码

- 为什么自强的小程序开发基本都基于Uniapp?
	- 开发统一基于Vue这一成熟的框架语法
	- 组件，UI生态丰富，跨端适配性好

</div>


<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## Uniapp概论

一个Uniapp项目长什么样？

<div class="fragment" style="margin-top: 40px">

### 顶层结构

* `pages/`：页面（路由对应的单页）
* `components/`：通用组件（按钮、弹窗、列表卡片等）
* `static/`：静态资源（图片、icon、字体等）
* `common/` 或 `utils/` 或 `js/`：公共 JS 函数、请求封装、工具方法
* `App.vue`：应用入口，定义全局样式、根组件
* `main.js`：入口 JS，注册全局组件、挂载应用
* `pages.json`：配置路由、tabBar、页面路径等（Uniapp 特有）

</div>

<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## Uniapp概论

关于`pages`(页面)

<div class="fragment" style="margin-top: 20px">

1. 页面是什么？
   * 对应用户看到的“完整一屏/一个功能场景”
   * 在 Uniapp 中，一般一个路由 = 一个 `pages` 下的页面文件夹

</div>
<div class="fragment" style="margin-top: 20px">

2. 页面文件结构（基于 Vue 的单文件组件思想）

   * 模板：`<template>` 对应 HTML
   * 脚本：`<script>` 对应 JS（数据、生命周期、方法）
   * 样式：`<style>` 对应 CSS

</div>
<div class="fragment" style="margin-top: 20px">

3. 和“后端页面”的区别

   * 后端页面更多是“请求一次，渲染一次”
   * 前端单页/小程序页面是长生命周期、频繁交互，更依赖组件 & 状态管理

</div>

<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## Uniapp概论

关于`components`(组件)
<div class="fragment" style="margin-top: 20px">

1. 组件是什么？
   * 可以复用的 UI + 逻辑组合块
   * 比如：搜索框组件、商品卡片组件、弹窗组件

</div>
<div class="fragment" style="margin-top: 20px">

2. 组件的作用
   * 拆分大页面：一个页面拆成多个小模块，降低复杂度
   * 复用：多个页面用同一套 UI，而不是复制粘贴

</div>
<div class="fragment" style="margin-top: 20px">

3. 组件和页面的区别
   * 页面通常对应一个路由，有独立生命周期
   * 组件通常嵌套在页面里，被页面或其他组件使用

</div>

<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## Uniapp概论

关于`static`(静态资源)
<div class="fragment" style="margin-top: 20px">

1. 静态资源定义
   * 项目中不会“编译生成”的文件：图片、字体、svg 图标、静态 json 等

</div>
<div class="fragment" style="margin-top: 20px">

2. 为什么要单独放
   * 方便管理、打包、缓存
   * 打包构建时可以做路径、Hash 处理，利于浏览器缓存

</div>
<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## Uniapp概论

关于`js / common / utils`(公共逻辑)

<div class="fragment" style="margin-top: 20px">

1. 通用工具函数
   * 比如时间格式化、节流防抖、校验工具

</div>
<div class="fragment" style="margin-top: 20px">

2. 请求封装
   * 对 `uni.request` 或 `wx.request` 进行封装
   * 统一处理：baseURL、请求头、错误码、token 过期等

</div>
<div class="fragment" style="margin-top: 20px">

3. 全局常量 & 配置
   * 接口地址、环境变量（开发/测试/生产）、通用枚举等

</div>

<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## Uniapp概论

一个成熟前端项目中的关键因素

- 页面
- 组件
- 静态资源
- 数据流
- 缓存
- 后端接口

<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## Uniapp概论

关于数据流

<div class="fragment" style="margin-top: 20px">

1. 单向数据流概念

   * 数据从上层组件 → 下层组件传递（props）
   * 事件从下层组件 → 上层组件传递（自定义事件）

</div>
<div class="fragment" style="margin-top: 20px">

2. 本地状态 OR 全局状态
   * 本地：某个页面/组件内部用的 `data`
   * 全局：例如登录用户信息、token、全局配置，可能用 `Vuex/Pinia` 或 Uniapp 的全局数据

</div>
<div class="fragment" style="margin-top: 20px">

3. 和后端数据的关系
   * 前端只是“数据消费者 + 展示者”
   * 通过接口拿到数据 → 存到状态 → 渲染页面

</div>

<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## Uniapp概论

关于缓存

<div class="fragment" style="margin-top: 20px">

1. 为什么要缓存

   * 提升性能，减少重复请求
   * 离线/弱网时也能显示部分内容

</div>
<div class="fragment" style="margin-top: 20px">

2. 常见缓存方式
   * 内存缓存：变量、全局状态（刷新页面就没了）
   * 本地存储：`uni.setStorage`、`localStorage` 等（刷新还在）

</div>
<div class="fragment" style="margin-top: 20px">

3. 需要注意的问题
   * 缓存过期策略（时间 / 版本号）
   * 隐私数据（token、用户信息）的安全存储

</div>

<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## Uniapp概论

关于API

<div class="fragment" style="margin-top: 20px">

1. 接口在前端项目中的角色

   * 前端不直接操作数据库，通过 HTTP/HTTPS 调用后端 API
   * 后端负责：鉴权、业务逻辑、数据存储、权限控制

</div>
<div class="fragment" style="margin-top: 20px">

2. 一次典型请求流程

   * 页面生命周期钩子中发请求（如 `onLoad`）
   * 请求封装层统一调用接口
   * 成功：更新页面/全局数据 → 视图自动更新
   * 失败：错误提示、重试、跳转登录等

</div>
<div class="fragment" style="margin-top: 20px">

3. 接口与 Mock

</div>

<!-- v -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

## 如何使用AI-IDE进行项目的上手与开发

- 配置好提示词/Rule
- 确认好UI
- 分析项目结构 明确需求要素
- 逐步有序开始开发
- 做好Debug

<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

<br>
<br>
<br>
<br>
<br>

<center><h5 style="font-size: 55px; text-align: center;">演示</h5></center>


<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

<br>
<br>
<br>
<br>
<br>

<center><h5 style="font-size: 55px; text-align: center;">Q&A</h5></center>



<!-- s -->
<!-- .slide: data-background="zqfrontend-lec-2/background.webp" -->

<br>
<br>
<br>
<br>
<br>

<center><h5 style="font-size: 55px; text-align: center;">感谢参与本次组会~</h5></center>
