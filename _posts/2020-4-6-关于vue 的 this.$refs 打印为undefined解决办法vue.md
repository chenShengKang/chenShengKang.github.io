---
layout:     post                    # 使用的布局（不需要改）
title:      vue               # 标题 
subtitle:   vueg #副标题
date:       2020-04-01              # 时间
author:     BY                      # 作者
header-img: img/post-bg-2015.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - 难题
    - vue
    - javascript
---

## 关于vue 的 this.$refs 打印为undefined解决办法
用ref 注册子组件，父组件可以通过this.$refs.xx.fn调用子组件里的函数，但是有时会出现 fn 为定义的情况，这是为什么呢？

vue 官网中ref 下有一段话  "关于 ref 注册时间的重要说明：因为 ref 本身是作为渲染结果被创建的，在初始渲染的时候你不能访问它们 - 它们还不存在！$refs 也不是响应式的，因此你不应该试图用它在模板中做数据绑定。"

也就是说 ref 只有等页面加载完成好之后你才能调用 this.$refs ，如果你使用v-if 、v-for渲染页面的话，那么在刚开始页面没没渲染之前你是拿不到this.$refs 的，所以要等到页面渲染之后拿才可以



      mounted() {
         setTimeout(() => {
           this.pushTitle()  
         },16),
        //在 nextTick 还是无法获取加过 if 判断的内容
       // this.$nextTick(() => {
       //     this.pushTitle()  
       //})
      }



