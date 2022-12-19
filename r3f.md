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
