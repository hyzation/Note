# REACT
### 使用swiper ###
```
//  安装版本：8.0.1
yarn add swiper

//  引入所需模块 （不要忘了css）
import { Autoplay, Pagination, Mousewheel, Navigation, Thumbs } from 'swiper'
import { Swiper, SwiperSlide } from 'swiper/react';
import 'swiper/css';

<Swiper
    modules={[Autoplay, Pagination, Mousewheel, Navigation, Thumbs]}
    thumbs={{ swiper: thumbsSwiper }}   //使用模块
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
```
