# html+css

[toc]{level: [2]}

## 前端SEO优化
- **title、alt、h1**：title：网站头部标签head下的title,网站名称。alt: 当网络速度很慢，或者图片地址失效的时候，它可以在图片展示的位置上显示该图片的名称。h1：h1标签自带权重“蜘蛛” 认为它最重要，一个页面有且最多只能有一个h1标签，放在该页面最重要的标题上面，如首页的logo上可以加H1标签。副标题用 标签, 而其它地方不应该随便乱用 h 标题标签。

## 文字超出省略 ##
```
{
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
}
```
