# vue
## 字符串拼接变量
```
<image class="tag5" :src="`../../static/images/level-${level}@2x.png`" mode=""></image>
```
## $emit 报警告
```
[Vue warn]: Extraneous non-emits event listeners (changeParentProps) were passed to component but could not be automatically inherited because component renders fragment or text root nodes. If the listener is intended to be a component custom event listener only, declare it using the “emits” option.
//在子组件声明
export default {
    emits: ['metapoint'],   //emit的方法
}
```
