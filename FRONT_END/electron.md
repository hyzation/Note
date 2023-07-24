# electron
## 官中文档 https://www.electronjs.org/
## yarn报错 'command falid'
```
yarn config set electron_mirror https://npm.taobao.org/mirrors/electron/
yarn add --dev electron
```
## 开发者控制台
首先顶部菜单栏不能关 这行：Menu.setApplicationMenu(null) 
默认 ctrl+shift+I
## 打包
暂时只能打包当前平台的应用
```
yarn run make
```

