# React

## 创建React应用
```
npx create-react-app my-app
cd my-app
yarn start
----------
react-router-dom    //router
antd    //antd
```

## 使用jsx
Jsx的全称是Javascript XML，react定义的一种类似XML的JS拓展语法：JS+XML。本质是React.createElement(component, props, ...children) 的语法糖。
- 在src下创建app.jsx, 入口文件index.js引入app.jsx


## 使用swiper
- **中文博客** https://blog.csdn.net/supming1/article/details/108204052
- **官英文档** https://swiperjs.com/react
```
//  安装版本：8.0.1
yarn add swiper

//广告双轮播案例👇

//  引入所需模块 （不要忘了css）
import { useState } from "react"    //为了下面用thumbs
import { Autoplay, Pagination, Mousewheel, Navigation, Thumbs } from 'swiper'
import { Swiper, SwiperSlide } from 'swiper/react';
import 'swiper/css';

const [thumbsSwiper, setThumbsSwiper] = useState(null);

<Swiper
    modules={[Autoplay, Pagination, Mousewheel, Navigation, Thumbs]}    //使用模块
    thumbs={{ swiper: thumbsSwiper }}   //广告轮播图thumbs
    style={{ width: '100%', height: '100%', }}  //设置宽高
    navigation={{   //navigation可自定义
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
        disabledClass: 'disable' // 当导航按钮变为不可用时添加的class,也就是当swiper索引为0时上一张没有prevEl的class类名就会添加一个disable，也就是.swiper-button-prev .disable
    }}
    autoplay={{ //自动轮播
        delay: 0,   //想要无阻塞滚动这里要设置0
        disableOnInteraction: false, // 鼠标移出是否继续滚动
        pauseOnMouseEnter: false, // 鼠标移入暂停
        reverseDirection: false,    //反向播放
    }}
    slidesPerView={1}   //屏幕显示多少张
    speed={800}    //轮播速度
    mousewheel={true}   //鼠标滚轮操作
    loop    //头尾衔接
    allowTouchMove={false}  //禁用拖拽
    direction="vertical"    //滚动方向，默认horizontal 

>

    {
        swiperbanner.map((item, index) => {
            return <SwiperSlide className="busSwiperBox" key={index}>
                <img src={item.img} alt="" />
            </SwiperSlide>
        })
    }
    <div className="swiper-button-prev">上一个</div>
    <div className="swiper-button-next">下一个</div>
</Swiper>

{/* Thumbs Swiper -> store swiper instance */}
<Swiper
    modules={[Pagination, Mousewheel, Thumbs]}
    onSwiper={setThumbsSwiper}  //广告轮播图thumbs
    style={{ width: '100%', height: '20%', borderTop: '3px solid #eee', paddingTop: '5px', }}
    slidesPerView={5}
    spaceBetween={5}
    speed={600}
    mousewheel={true}
    loop
    allowTouchMove={true}
>
    {
        swiperbanner.map((item, index) => {
            return <SwiperSlide className="busSwiperBox" style={{ border: '1px solid #eee', }} key={index}>
            <img src={item.img} alt="" />
            </SwiperSlide>
        })
    }
</Swiper>
```
