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

