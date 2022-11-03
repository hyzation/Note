# nextJS
## 官中文档 https://nextjs.frontendx.cn/
## “window is not defind”
next.js是服务器渲染，运行在node上的，并不是浏览器上的；
需要使用生命周期componentDidMount，或者在useEffect中调用。
## 导入使用自定义字体
```
<!-- 1.创建font.css文件并引入 -->
@font-face {
    font-family: qiantubifeng;  //自定义名称
    src: url('/fonts/qiantubifeng.ttf');
}

<!-- 2.在_app.js中引入css文件 -->
import '../styles/font.css';

<!-- 3.字体使用 -->
text{
    font-family: qiantubifeng;
}
```
