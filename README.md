## javascript 知识备忘录
### 正则表达式

- [强烈推荐老姚的正则表达式 ⭐️⭐️⭐️⭐️⭐️](https://juejin.im/post/5965943ff265da6c30653879)
-------

### 异步处理能力
- [谷歌开发者文档-promise ⭐️⭐️⭐️⭐️⭐️](https://developers.google.com/web/fundamentals/primers/promises?hl=zh-cn)
- [更快的 async 函数和 promises](https://juejin.im/post/5beea5f5f265da61590b40cd?utm_source=gold_browser_extension)

-------

### EventLoop
- [JavaScript 运行机制详解：再谈Event Loop](http://www.ruanyifeng.com/blog/2014/10/event-loop.html)

-------

### webpack/babel
- [webpack中文 ⭐️⭐️⭐️⭐️⭐️](https://webpack.docschina.org)
- [babel官网 ⭐️⭐️⭐️⭐️⭐️](https://babeljs.io/)

- [细说 webpack 之流程篇](http://taobaofed.org/blog/2016/09/09/webpack-flow/)
- [contributors-guide](https://medium.com/webpack/contributors-guide/home)
- [astexplorer](https://astexplorer.net/)
- [玩转webpack（一）上篇：webpack的基本架构和构建流程](https://cloud.tencent.com/developer/article/1006353)
- [Webpack 源码解析](https://github.com/lihongxun945/diving-into-webpack)
- [Babel 手册](https://github.com/jamiebuilds/babel-handbook/tree/master/translations/zh-Hans)
- [babael插件编写](https://www.cnblogs.com/chyingp/p/how-to-write-a-babel-plugin.html)
- [diving-into-webpack](https://github.com/lihongxun945/diving-into-webpack)


-------

### puppeteer

-------
### docker

-------
### nginx

-------
### 算法
- [记录前端开发中的技巧以及算法知识](https://github.com/louzhedong/blog)
[minipack-explain](记录前端开发中的技巧以及算法知识)
-------
### node

-------
### git
- [可视化，Git进阶 ⭐️⭐️⭐️⭐️⭐️](https://learngitbranching.js.org/)
- [Git飞行规则 ⭐️⭐️⭐️⭐️⭐️](https://github.com/k88hudson/git-flight-rules/blob/master/README_zh-CN.md)
-------
### 数据库

-------
### typescript

-------
### 常用库源码分析

-------


### 服务端渲染
- [React 中同构（SSR）原理脉络梳理](https://juejin.im/post/5bc7ea48e51d450e46289eab)


-------

### V8
- [深入理解 V8 的 Call Stack](https://mp.weixin.qq.com/s?__biz=MzU0Nzk1MTg5OA==&mid=2247483967&idx=1&sn=b8282dc5a672df7345281ce67841cf0d&chksm=fb47c64acc304f5c5d1f1e140285dbff67a888f1dd0387b589002902ffeb26e59e550d0323e7&scene=21#wechat_redirect)

```javascript
console.log('main1');
setTimeout(function() {
    console.log('setTimeout');
    process.nextTick(function() {
        console.log('process.nextTick2');
    });
}, 0);

new Promise(function(resolve, reject) {
    console.log('promise');
    resolve();
}).then(function() {
    console.log('promise then');
});

process.nextTick(function() {
    console.log('process.nextTick1');
});
console.log('main2');
```