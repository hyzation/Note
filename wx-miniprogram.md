# miniprogram
## 监听设备方向变化事件（类似陀螺仪）
```
wx.onDeviceMotionChange((result) => {
    // console.log('设备方向：', result); //alpha,beta,gamma
    gamma 控制左右 左正右负
    beta 控制上下 上正下负
    alpha 控制旋转
})
```
## object-fit 不起作用
小程序不支持object-fit样式； 用mode属性，如 mode="aspectFill"
官方文档：https://developers.weixin.qq.com/miniprogram/dev/component/image.html#属性说明