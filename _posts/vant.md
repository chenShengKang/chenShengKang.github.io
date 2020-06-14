---
layout:     post                    # 使用的布局（不需要改）
title:      My second Post               # 标题 
subtitle:   Hello World, Hello Blog #副标题
date:       2020-02-06              # 时间
author:     BY                      # 作者
header-img: img/post-bg-2015.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - 生活
---
### 统一导入

~~~js
// pluginit => vant.js
// 统一导入，并引入
import Vue from 'vue'
import {
    Button,
    NavBar,
    Tabbar,
    TabbarItem,
    Swipe,
    SwipeItem,
    Sticky,
    GoodsAction,
    GoodsActionIcon,
    GoodsActionButton,
    Toast,
    Card,
    SubmitBar,
    Checkbox,
    Icon,
} from 'vant'

Vue.use(Button);
Vue.use(NavBar);
Vue.use(Tabbar);
Vue.use(TabbarItem);
Vue.use(Swipe);
Vue.use(SwipeItem);
Vue.use(Sticky);
Vue.use(GoodsAction);
Vue.use(GoodsActionIcon);
Vue.use(GoodsActionButton);
Vue.use(Toast);
Vue.use(Card);
Vue.use(SubmitBar);
Vue.use(Checkbox)
Vue.use(Icon)

~~~

### 引入

~~~js
// main.js  引入
//引入 vant ui
import './pluginunit/vant.js'
~~~

