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
## 打包
```
npx next build 
npx next export
```
## 使用swiper时delay: 0,不生效
```
/* 取消停顿 */
.swiper-wrapper {
    transition-timing-function: linear !important;
}
```
## 引入移动端适配库postcss-pxtorem (屏幕自适应)
```
<!-- 详见nine_world_3d_next项目，参考自https://zhuanlan.zhihu.com/p/382916768 -->
1.安装模块
yarn add amfe-flexible
yarn add -D postcss-pxtorem

2.在项目根目录创建postcss.config.js文件
module.exports = {
  plugins: { 
    'postcss-pxtorem': {
      rootValue: 1080 / 10,  // 1080px为设计稿大小
      unitPrecision: 5,
      propList: ["*"],
      selectorBlackList: [/^.html/], //排除html样式
      replace: true,
      mediaQuery: false,
      minPixelValue: 0
    }
  }
}

3.写个全局组件引用amfe-flexible
import React, { useEffect } from "react";
import Head from "next/head";

export default function Global() {
    useEffect(() => {
        import("amfe-flexible");
    }, []);
    return (
        <div>
            <Head>
                <title>苏州九界传媒</title>
                <meta name="description" content="苏州九界传媒" />
                <meta name="keywords" content="苏州九界传媒" />
                <meta charSet="UTF-8"></meta>
                <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, minimum-scale=1, user-scalable=no"></meta>
            </Head>
        </div>)
}

4.在_app.js中引入该全局组件
import Global from "../src/components/Global/Global";
export default function MyApp({ Component, pageProps }) {
    return <>
        <Global />
    <>
}
```

