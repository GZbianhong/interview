# Q
###纸笔测试
### 1. 重写如下代码，得到**相同运行效果**
```javascript
console.log(foo); 
var foo = 2;
```


### 2. 数组去重
```javascript
let rd=Array.apply(null,Array(10))
    .map(function(){
        return parseInt(10*Math.random())
    });
console.log(rd);//[5, 8, 1, 1, 8, 5, 7, 4, 4, 8]
```

根据以上信息，请使用至少两种方式，实现 rd 数组元素去重，**并显示代码耗时**。



### 3. 写出以下代码的输出结果

- A
```javascript
const a=[9,12,4,30,...[8,33,49]];
let b=a.slice();
let c=a;
c.reverse();
b.pop();
console.log(a,b,c)
```
- B
```javascript
let str="may the force be with you";

console.log(str.replace(/[\s]/,'_'))

console.log(str.replace(/[\s]*/,'_'))

console.log(str.replace(/[\s]/g,'_'))

console.log(str.replace(/[\S]/g,'_'))

console.log(str.replace(/[\S]/,'_'))

```
- C
```javascript
let np=()=>{
    return new Promise((res,rej){
        res(true);
        rej(false);
    })
};
np()
.then(msg=>{console.log(msg)})
.catch(msg=>{console.log(msg)});
```
---
- D
```javascript
let add=num=>{return n=>{return num+n}};
let add_3=add(3);
console.log(add_3(.5))
```
###上机测试

### 1. 使用闭包，实现一个简单的计数器。

### 2. 实现一个函数sum()
```javascript
let sum=string=>{
    //your code
}
console.log(sum('.1,.2')===0.3);//true;
console.log(sum('0.1,0.2')===0.3);//true;
console.log(sum('0.1,0.2,0.4,0.08')===0.78);//true;
console.log(sum('0.1,0.2,0.4,0.008')===0.708);//true;
```

### 3. 使用MongoDB、Express，实现如下需求：

- 用户注册
- 用户登录
- 用户授权

>状态与信息
【登录】0：成功，1：该手机号码没有注册，2：手机号与密码不匹配。
【注册】0：成功，1：该手机号码已注册。


>路由
【登录页面】/login
【注册页面】/register
【授权页面】/auth
【查询页面】/query


>数据
【A】{"stat":"0","msg":"succ"}
【B】{"stat":"1","msg":"unauthorized"}


使用HTML+JS搭建简单的登录注册页面，请求通过ajax异步提交实现。
后端判别后返回登录状态与信息，前端提示返回信息后跳转到授权页面。


授权页面显示两个按钮，一个为授权，另一个为不授权。默认为不授权。
点击授权后显示一段access_token。

用户授权后，可用GET method 带access_token在查询页面请求到数据【A】。
如果用户没有授权，使用access_token会返回数据【B】.

---

