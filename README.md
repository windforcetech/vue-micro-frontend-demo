## Vue前端微服务基座工程

## 为什么产生这个Demo
演示庞大的SPA如何进行子应用的拆分，一个小小的微前端理念实践，按需加载，最终实现按需增量发布,默认只加载基站项目,然后根据子业务路由，按需加载对应的入口文件，无论 `react`,`vue`还是传统的`backbone`的项目，都大同小异的实现

## 核心原理
> 基座工程将vueRouter的实例挂载在全局，然后各个子项目的app.js加载完成后，注册自己的路由，然后vueRouter重新访问当前路由，还有一种做法是，vue访问的路由，内部是异步组件，在异步组件内部拿到 组件，可以参考美团外卖的这个实践 https://mp.weixin.qq.com/s/l17Uo6Q7up44uZI_VojFzw



## 快速开始

(1) 安装依赖

```
 npm i
```

(2)本地开发

```
npm run dev
```

(3) 追加子项目
> 按照 src/subapp 下子目录的 `bi-report` 的目录结构，可以追加新工程，然后移动端的BI所有工程合成一个超级工程，然后每次按需发布基座工程 index.js 或者子应用的入口文件

