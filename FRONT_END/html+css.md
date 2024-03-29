# html+css

[toc]{level: [2,3]}

## 前端SEO优化
- **title、alt、h1**：title：网站头部标签head下的title,网站名称。alt: 当网络速度很慢，或者图片地址失效的时候，它可以在图片展示的位置上显示该图片的名称。h1：h1标签自带权重“蜘蛛” 认为它最重要，一个页面有且最多只能有一个h1标签，放在该页面最重要的标题上面，如首页的logo上可以加H1标签。副标题用 标签, 而其它地方不应该随便乱用 h 标题标签。

## web端适配移动端
宽高字体使用px转vw，如1920宽屏，某元素的长度为24px，使用 100/1920*24；
或meta标签
```
<meta name="viewport" content="width=device-width, initial-scale=1">
```

## 文字超出省略...
```
{
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
}

//只显示一行
{
    white-space: nowrap; 
    width: 100%; 
    overflow: hidden;
    text-overflow:ellipsis;
}
```

## 常用文字样式
```
{
    writing-mode: vertical-lr;  //文字竖向排列
    text-indent: 2em;   //首行缩进
    text-transform: uppercase;  //全部大写；capitalize首字母大写；lowercase全部小写
    -moz-user-select: none;  //所属元素的文字不可选中；下同理
    -webkit-user-select: none;
    user-select: none;
}
```
## 文字撑满元素（类似flex布局的space-between）
```
  .kidp3 {
    width: 250px;
    text-align: justify;
    text-justify: distribute-all-lines;
    text-align-last: justify;
}
```
## input
```
autocomplete="off"  //禁止自动填充
```
## 深色png变白
```
filter: invert(1) brightness(2);
```
## 常用grid布局
```
{
    display: grid;  //开启grid
    grid-template-columns: repeat(3, 30%);  //定以列
    grid-template-rows: repeat(auto-fill, 100px);   //定以行
    place-content: space-between;   //每个单元格排列
    place-items: center;    //单元格内容
}
```
## 去掉指定元素滚动条
```
.yourClassName::-webkit-scrollbar{
    display: none;
}
```
## 滚动条样式
```
::-webkit-scrollbar {
    /*滚动条整体样式*/
    width: 8px;
    /*高宽分别对应横竖滚动条的尺寸*/
    height: 1px;
    /* display: none; */
}

::-webkit-scrollbar-thumb {
    /*滚动条滑块样式*/
    border-radius: 10px;
    box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2);
    background: #ddd;
    transition: all 0.5s;
}

::-webkit-scrollbar-thumb:hover {
    /* hover上去后的滚动条滑块样式 */
    background-color: #bbb;
}

::-webkit-scrollbar-track {
    /*滚动条背景样式*/
    box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2);
    /* border-radius: 10px; */
    background: #eee;
}

::-webkit-scrollbar-track:hover {
    /* hover上去后的滚动条背景样式 */
    background-color: #eee;
}
```
## 元素选择
```
//选择元素中除最后一个之外的所有子元素
element:not(:last-child) { }
```
## css类选择器逗号、空格、连写的区别
```
.name1,.name2 {} // 逗号表示当前元素具备其中一个就会出现效果
.name1 .name2 {} // 空格表示从属包含关系，前元素的子元素才会出现效果
.name1,.name2 {} // 连写表示需要同时具备才会出现效果
```
