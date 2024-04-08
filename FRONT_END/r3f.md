# r3f
## 安装
```
three
@react-three/fiber
@react-three/drei
```
## Canvas配置
```
<Canvas 
    style={{ width: '100vw', height: '100vh' }}
    camera={{ position: [10, 10, 10], zoom: 10, }}  //相机位置，纵深（远近）
    orthographic    //相当于drei的OrthographicCamera
    shadows //阴影
    dpr={[1, 2]}    //像素比
>
</Canvas>
```
## MapControls
- 像拖拽地图一样的拖拽视角
```
 <MapControls
    screenSpacePanning  //true拖拽会改变角度；false不会改变角度
    ref={ref}
    onChange={handleChange}
    enableDamping={true}
    dampingFactor={0.05}
    minDistance={100}
    maxDistance={500}
    maxPolarAngle={Math.PI / 2}
    enableZoom={false}
    enableRotate={true}
/>
```

## 资源占用显示
```
import { Perf } from "r3f-perf";
<Perf position='bottom-right' />
```

## 坐标系
```
<axesHelper args={[5]} />
```

## OrbitControls属性
```
autoRotate：一个布尔值，指定是否启用自动旋转。默认值为 false。
autoRotateSpeed：自动旋转的速度。默认值为 2。
dampingFactor：阻尼系数，用于平滑移动。默认值为 0.05。
enableDamping：一个布尔值，指定是否启用阻尼。默认值为 true。
enableKeys：一个布尔值，指定是否启用键盘控制。默认值为 true。
enablePan：一个布尔值，指定是否启用平移控制。默认值为 true。
enableRotate：一个布尔值，指定是否启用旋转控制。默认值为 true。
enableZoom：一个布尔值，指定是否启用缩放控制。默认值为 true。
keyPanSpeed：平移控制的速度。默认值为 7。
maxAzimuthAngle：最大方位角，以弧度为单位。默认值为 Infinity。
maxDistance：最大距离。默认值为 Infinity。
maxPolarAngle：最大极角，以弧度为单位。默认值为 Math.PI。
minAzimuthAngle：最小方位角，以弧度为单位。默认值为 -Infinity。
minDistance：最小距离。默认值为 0。
minPolarAngle：最小极角，以弧度为单位。默认值为 0。
rotateSpeed：旋转控制的速度。默认值为 0.3。
zoomSpeed：缩放控制的速度。默认值为 1。
```

