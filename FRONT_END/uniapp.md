# uniapp
## 官方文档 https://uniapp.dcloud.net.cn/
## 去除滚动条
```
App.vue:
scroll-view ::-webkit-scrollbar {
    display: none !important;
    width: 0 !important;
    height: 0 !important;
    -webkit-appearance: none;
    background: transparent;
}
```
## 页面滚动据顶部距离
```
<!-- 生命周期 -->
onPageScroll(e) {
    // 传入scrollTop值并触发所有easy-loadimage组件下的滚动监听事件
    // this.scrollTop = e.scrollTop;
    console.log(111);
},
```
## 判断是否是ios
```
let u = navigator.userAgent;
let isiOS = !!u.match(/\(i[^;]+;( U;)? CPU.+Mac OS X/); //ios终端
console.log(isiOS);
```
