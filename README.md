# Vue.js的学习经验总结
> 个人经验总结，或许不全不精确，欢迎交流经验，相互学习，相互提升。

## 目录:
#### 1. [Vue 简介](#divtop1)
#### 2. [Vue 的入门 demo](#divtop2)

## 1.Vue 简介
<div id="divtop1"><div>
Vue 是一个前端的双向绑定类的框架，发音[读音 /vjuː/, 类似于 [view]。新的 Vue 版本参考了 React 的部分设计，当然也有自己独特的地方，比如 Vue 的单文件组件开发方式都很有创新，另外 Vue 自身的一些绑定的语法、用法等都非常精炼，很容易上手，而且第三方的插件都非常丰富，社区非常活跃，最新的文档都有中文版本。而且 Vue 配合官方的和第三方的库可以实现单文件的组件化开发、SPA 等现代化前端开发。
详情请参考Vue 官网

## 2.Vue 的入门 demo 
<div id="divtop2"><div>
Vue 可以直接把它当做一个 js 库使用，所以它可以很容易的接入到你的项目或者单个页面中。甚至你可以只使用它的双向绑定功能。所以它很容易上手。

下面开始我们的第一个demo

```html
第一步： 在根目录创建一个html文件 比如：index.html.

第二步：引入Vue库
<script src="https://unpkg.com/vue/dist/vue.js"></script>
当然了你可以直接下载Vue的js文件，推荐你直接用上面的cdn即可。

第三步：创建一个Div，给它一个id，比如：app

第四步：创建Vue的对象，并把数据绑定到上面创建好的div上去。
```

书写代码如下：
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <!-- 1.先引入 Vue库 -->
    <script src="https://unpkg.com/vue/dist/vue.js"></script>
    <title>vue入门实例</title>
</head>

<body>
    <!-- 2.创建一个div -->
    <div id="app">
        <!--Vue的模板的绑定数据的方法， 类似于很多其他前端的模板，可以用两对花括号进行绑定Vue中的数据对象的属性 -->
        {{message}}
    </div>
    <script>
        // 3：创建Vue的对象，并把数据绑定到上面创建好的div上去
        new Vue({ // 创建Vue对象。Vue的核心对象。
            el: '#app', //el是element的简写。el属性：把当前Vue对象挂载到 div标签上，#app是id选择器
            data: { // data: 是Vue对象中绑定的数据
                message: 'hello Vue!' // message 自定义的数据
            }
        });
    </script>
</body>

</html>
```

