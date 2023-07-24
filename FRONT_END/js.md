# js
### ?? 与 ?.运算符
```
let obj = { name: 'tktk,}
// obj?.name 类似于 obj.name (?.)会加判断obj是否包含name属性
// obj.name??'tktk' 类似于 obj.name? 'obj.name': 'tktk 同样会加一层判断
```
## 原生JS复制内容
```
navigator.clipboard.writeText(value).then(() => {
    console.log(value); //value为复制的内容
});
```
## 获取元素
```
document.querySelectorAll('.classname') //获取class为classname的所有元素
```
## 获取页面各距离
```
let currentH = document.documentElement.clientHeight    //屏幕高度
let scrollH = document.documentElement.scrollTop    //滚动距顶部距离
```

