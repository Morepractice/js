# js学习

* 刷新页面

1. 使用*reload(flag)*,flag默认为true,当为true时，以get方式从服务器获取页面并刷新,当为false时,则从浏览器获取页面刷新;

2. 使用*replace(url)*,将以新的url代替原来的页面,与*location = 'url'*的区别为此种方式不可回退到原来的页面;

3. 其它页面刷新方式;

```js
history.back(); //退回上一个页面
history.go(-1); //-1代表上一个页面，1代表下个页面，依此类推

```

4. 自动刷新页面;

```js
function refreshPage(){
    window.location.reload();
}

setTimeOut(refreshPage,1000);//也可使用setInterval方法，单位ms
```

5. setInterval与setTimeout区别:

setInterval为每隔一段时间执行一次即执行无限次,setTimeout代表隔几秒执行一次;最小执行时间,setInterval为10ms,setTimeout为4ms

```js
function fn(){
    console.log(111);
}

setInterval(fn,1000);

//相当于(区别：)

setTimeout(function fn(){
    console.log(111);
    setTimeOut(fn,1000);
})
```
