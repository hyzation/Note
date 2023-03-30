# yarn+npm+pnpm
### 更新依赖
```
第一种
yarn upgrade-interactive --latest
# 需要手动选择升级的依赖包，按空格键选择，a 键切换所有，i 键反选选择

第二种
yarn upgrade package@version
# yarn.lock和package.json都会更新，但是会进行版本锁定 "echarts": "4.2.0-rc.2"
```
