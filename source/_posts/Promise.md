---
title: Promsie
date: 2021-10-28
tags:
- JavaScript
- Prosmise
categories: JavaScript
---

### 期约基础
ECMAScript6新增的引用类型`Promise`可以通过`new`操作符来实例化。创建期约需要传入执行器(`executor`)函数作为参数
下面的例子使用一个空对象来应付一下解释器:
```
let p = new Promise(()=>{});
setTimeout(console.log,0,p) // Promise <pending>
```
1、期约状态机
在把一个期约实例传递给`console.log()`时，(控制台输出)表明该实例处于待定(pending)状态，期约是一个有状态的对象。
期约是一个有状态的对象:
- 待定(pending)
- 兑现(fulfilled,resolve)
- 拒绝(rejected)
待定(pending) 是期约的初始状态。在待定状态下，期约可以落定 为代表成功的兑现(`fulfilled`)状态，或者代表失败的拒绝(rejected)状态。无论是哪种状态都是不可逆的。只要从待定转为兑现或拒绝,期约的状态就不在改变。

