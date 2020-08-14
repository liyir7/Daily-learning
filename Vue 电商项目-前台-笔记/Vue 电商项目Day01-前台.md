# Vue 电商项目-前台

# Day01-前台

## 项目简介

#### 	前台PC三大项目

- 电商
- 物流
- 金融

### 模块化  + 组件化 = 工程化

#### 模块化

1. 模块代表是一个文件
2. 模块化代表是一个项目(一个JS文件)

#### 组件化

1. 组件代表一个一个的 .vue 文件
2. 组件化是一个一个 .vue文件组成的项目

### 面试

​	1) 此项目为在线电商Web App (SPA)

​	2) 包括首页, 搜索列表, 商品详情, 购物车, 订单, 支付, 用户登陆/注册	等多个子模块

​	3) 使用Vue全家桶+ES6++Webpack+Axios等前端最新最热的技术

​	4) 采用模块化、组件化、工程化的模式开发

### 前台数据处理交互组件化

1. ​	vuex  	共享数据状态体
2. ​	vue routher   路由器
3. ​	vue-lazyload    图片懒加载
4. ​	element-ui    后台用的%99都是element-ui
5. ​	swiper   专门的各式各样的轮播图插件
6. ​	moment    片刻,时间

### 前后台交互

#### ajax请求

1. ​	axios本质是一个函数  函数也是一个对象
2. ​	包含三种参数
   1. 可以做函数
   2. 可以做对象 
   3. 做函数返回值是一个promise对象

#### async/await

#### mock数据

​	mockjs 数据 模拟数据

#### 接口测试

​	postman 后端人员给接口,用postman先测试接口是否可以使用

### 模块化

#### 	Es6模块化

1. 引入
   默认暴露
   import add from 'xxx'
     统一暴露/分别暴露
   import { xxx, yyy as zzz } from 'xxx';
   import * as xxx from 'xxx';
2. 暴露
   export default xxx  默认暴露
     export {}           统一暴露
     export const xxx = xxx 分别暴露

### 项目构建/工程化

#### webpack

​	构建工具

#### vue-cli3 脚手架

	脚手架V2: 相对老的项目(了解了解)
	脚手架v3: 较新的项目
	脚手架v4: 最新的

1. vue-cli3和vue-cli4创建的项目不要找webpack的配置项目
2. 应为vue-cli3和vue-cli4创建的项目 webpack的配置项目全部被隐藏
3. 如果想改  创建vue.config.js文件

#### 使用vue的脚手架

	npm install -g @vue/cli    3的脚手架
	vue create vue-app3  
	
	npm install -g @vue/cli-init  2的脚手架
	vue init webpack vue-app2   
	
	npm install -g vue-cli  2的脚手架(老的, 现在不用了)
	vue init webpack vue-app2

#### 比较V2与V3创建的项目

```
1. v2的配置是直接可见, v3是包装隐藏起来了
2. 修改配置: v2是直接在配置文件中修改, v3提供了一个专门的配置: 	vue.config.js, 	我们可以根据文档在此文件中添加配置
3. vue使用的是不带编译器的版本, 打包文件更小  不写template配置, 直接render配置
```

### css预编译器

​	less

​	stylus

### 其他

lodash  工具函数包-含防抖节流深浅拷贝等......

store   存储方案

uuidjs

### 流程及开发方法

1. 熟悉一个项目的开发流程

2. 学会模块化、组件化、工程化的开发模式

3. 掌握使用vue-cli脚手架初始化Vue.js项目

4. 学会模拟json后端数据，实现前后端分离开发

5. 学会ES6+eslint的开发方式
6. 掌握一些项目优化技巧(webpack)

### Vue插件或第三方库

1. 学会使用vue-router开发单页应用

2. 学会使用axios与后端进行数据交互
3. 学会使用vuex管理应用组件状态
4. 学会使用swiper实现页面滑动效果
5. 学会使用elment-ui组件库构建界面

6. 学会使用vue-lazyload实现图片惰加载

7. 学会使用mockjs模拟后台数据接口

## Vue 电商项目-前台详解

### 脚手架创建项目

1. 创建文件夹-gulishop-client

2. 打开控制面板-路径cmd回车

3. 输入C:\Users\15040\Desktop\8.10LYR>vue create gulishop-client

4. 	1)	创建脚手架4/3的vue项目, 并运行
      		npm install -g @vue/cli
      		vue create vue-demo
      		npm run serve
      	
      	2)	创建脚手架2的vue项目
      		npm install -g @vue/cli-init
      		vue init webpack vue-demo
      		npm run dev

5. 配置完成跑起项目，没有报错各种都正常，证明项目准备没问题

   ```
   跑起来运行报错 （warning 找不到vue）  
   应为装的是3.0版本
   我们用的是2.6.11
   需要重新安装vue@2
   又找不到 vue-template-compiler
   安装 npm i vue-template-compiler -D
   ```

6. 

### 分析项目的主体架子

1. 观察页面确定页面主体框架
   - 所有的功能页面都是 上中下结构    上和下是不变化的，只有中间在变化   	
2. 定义页面主体组件组装，切换路径可以组件跳转（非路由组件和路由组件）
   1. Header和Footer是固定的所以是-非路由组件
   2. 、Home  Search  Login  Register 都是点击才会出现所以是-路由组件并且是一级的（可能内部还有二级）
   3. 非路由组件组装
   4. 路由组件注册使用 可以分模块去编写
3. 
4. 
5. 











