## javascript 基础知识
### 正则表达式

- [强烈推荐老姚的正则表达式](https://juejin.im/post/5965943ff265da6c30653879)
-------

### 异步处理能力
- [谷歌开发者文档-promise](https://developers.google.com/web/fundamentals/primers/promises?hl=zh-cn)
- [「译」更快的 async 函数和 promises](https://juejin.im/post/5beea5f5f265da61590b40cd?utm_source=gold_browser_extension)

-------

### EventLoop
- [JavaScript 运行机制详解：再谈Event Loop](http://www.ruanyifeng.com/blog/2014/10/event-loop.html)
- [Macrotask 与 Microtask 核心概念](http://js.walfud.com/macrotask-microtask/)
- [这一次，彻底弄懂 JavaScript 执行机制](https://juejin.im/post/59e85eebf265da430d571f89)
- [Nodejs 解读event loop的事件处理机制](https://www.jianshu.com/p/2a7ac1b3b382)
- [Node.js 代码阅读笔记系列 — process.nextTick() 的实现](https://juejin.im/post/58dc8533b123db006037c68c)
- [node，setImmeidate, setTimeout, nextTick你真的了解么？](https://hello2dj.github.io/2018/01/10/node%E5%AE%9A%E6%97%B6%E5%99%A8%E7%9B%B8%E5%85%B3%E8%AF%A6%E8%A7%A3/)

-------

### webpack/babel


-------

### puppeteer

-------
### docker

-------
### nginx

-------
### 算法

-------
### node

-------
### git

-------
### 数据库

-------
### typescript

-------
### rxjs

-------
### 常用库源码分析

-------


### 服务端渲染

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