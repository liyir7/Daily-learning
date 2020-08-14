# Vue 电商项目-前台

模块:js文件

模块化:项目

运行文件 npm run serve

### 前台数据处理交互组件化

​	vue routher

​	vuex

​	vue-lazyload  图片懒加载

​	element-ui  

​	swiper 专门的轮播图插件

​	moment

### 前后台交互

#### ajax请求

​	axios包含三种参数:可以做函数 可以做对象 做函数返回值是一个promise对象

​	async/await

#### mock数据

​	mockjs 数据 模拟数据

#### 接口测试

​	postman 后端人员给接口,用postman先测试接口是否可以使用

### 模块化

#### Es6模块化

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

webpack

vue-cli3 脚手架

	脚手架V2: 相对老的项目
	脚手架v3: 较新的项目
	脚手架v4: 最新的

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
2. 修改配置: v2是直接在配置文件中修改, v3提供了一个专门的配置: vue.config.js, 	我们可以根据文档在此文件中添加配置
3. vue使用的是不带编译器的版本, 打包文件更小  不写template配置, 直接render配置
```

### css预编译器

less

### 其他

lodash工具函数包-含防抖节流深浅拷贝等



### 流程及开发方法

1) 熟悉一个项目的开发流程

2) 学会模块化、组件化、工程化的开发模式

3) 掌握使用vue-cli脚手架初始化Vue.js项目

4) 学会模拟json后端数据，实现前后端分离开发

5) 学会ES6+eslint的开发方式

6) 掌握一些项目优化技巧(webpack)

### Vue插件或第三方库

1) 学会使用vue-router开发单页应用

2) 学会使用axios与后端进行数据交互

3) 学会使用vuex管理应用组件状态

4) 学会使用swiper实现页面滑动效果

5) 学会使用elment-ui组件库构建界面

6) 学会使用vue-lazyload实现图片惰加载

7) 学会使用mockjs模拟后台数据接口

### 项目流程

1. 创建文件夹

2. 路径输入cmd-打开控制面板

3. 控制面板输入

   ```
   vue create gulishop-client
   ```

4. 控制面板选择

   ```
   vue create vue-demo
   ```

5. 创建vue.config.js

   ```js
   module.exports = {
   // 1. vue-cli3和vue-cli4创建的项目不要找webpack的配置项目
   // 2. 应为vue-cli3和vue-cli4创建的项目 webpack的配置项目全部被隐藏
   // 3. 如果想改  创建vue.config.js文件
       lintOnSave: false,
     }
   
   ```

6. 创建jsconfig.json

   ```json
   {
       // 编译解析
       "compilerOptions": {
         "baseUrl": "./",
         "paths": {
             "@/*": ["src/*"]
         }
       },
       "exclude": ["node_modules", "dist"]
     }
   ```

7. 动了webpack文件就要重启项目

8. 建两个文件夹Footer， Header

   ![image-20200811203627306](C:\Users\15040\AppData\Roaming\Typora\typora-user-images\image-20200811203627306.png)

9. 辉洪 header  

10. npm install vue-router -s

11. 关联远程仓库

    1. 创建本地仓库git init
    2. 创建远程仓库
    3. 进行本地关联
    4. 本地有修改推送远程
    5. 本地有修改拉去本地
    6. 新员工直接克隆岛本地

12. 路由组建和非路由组建

    1. 注册方式不一样!!!
    2. 创建时期不一样(路由组建切换时要销毁,非路由组建一上来就创建了)

13. main.js注入router

    ![image-20200811142246973](C:\Users\15040\AppData\Roaming\Typora\typora-user-images\image-20200811142246973.png)

14. 切换浏览器地址(记录)方式

    - 路由导航链接
      - 声明式导航
      - <router-link to="/xxx">xxx</router-link>
    - 编程式导航链接
      - this.$router.push('/xxx')
      - this.$router.replace('/xxx')
      - this.$router.back()
      - this.$router.forward()

15. 写一个组建标签相当于创建了一个组件对象(每一个组建标签都会和每一个组件对象一一对应)

16. 跳转路由携带参数的2种方式
        	params参数
        	query参数
    	可以在路径后拼接  也可以使用对象写法

17. 路由传递仓库

    

18. 当传递参数有params参数的时候,对象写法必须是name和params

19. 遇见params用name

静态页面公用的文件夹

#### 接口测试

​	postman 后端人员给接口,用postman先测试接口是否可以使用

静态页面实现

​	拆分组件

​	组装组件

动态交互



scr文件里创建ajax文件夹

ajax文件夹里创建Ajax.js文件

Ajax.js文件

1. 我们发送ajsx请求的模块
2. 目的是为了对axios进行二次封装
3. 配置基础路径和超时限制
4. 添加进度条信息--nprogress
5. 返回响应不再需要从adta属性中拿数据



只要出现function就是新的内存

只要出现{}就是新的对象

只要出现新的[]就是新的数组

下载npm i axios -S

npm install --save vuex

```
npm install --save nprogress
```

三点运算符







