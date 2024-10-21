<div align="center">
  <img class="logo-light" width="520" src="https://alist.rikoneko.xyz/d/B2/site-img/koishi-uwu.png" alt="logo">
  <h1 id="koishi"><a href="https://github.com/RikoNeko/koishi-plugin-ygo-card-search" target="_blank">koishi-plugin-ygo-card-search</a></h1>
  <p>A YuGiOh card searching plugin for Koishi.</p>
</div>

[![npm](https://img.shields.io/npm/v/koishi-plugin-ygo-card-search?style=flat-square)](https://www.npmjs.com/package/koishi-plugin-ygo-card-search)

开发中的适用于Koishi的游戏王查卡插件，使用 [百鸽](https://ygocdb.com) 的API获取数据。

## 如何使用
命令`ck`或`查卡`后空格+卡名即可查询卡片信息。目前支持通过`-d`参数进行限定范围的搜索。

使用例：`ck 灰流丽`，`查卡 灰流丽`，`ck -d "不死族 调整" 灰流丽`，`查卡 -d "不死族 调整" 灰流丽`

## 卡片名称替换
替换规则的 JSON 文件格式如下：
```json
{
  "艾克佐迪亚": [
    "暗黑大法师",
    "黑暗大法师"
    ],
  "刻印群魔的刻魔锻冶师": [
    "刻魔"
    ]
}
```
前面的键是替换后的卡片名称，后面数组中的值是要被替换的卡片名称。

例如这里，暗黑大法师和黑暗大法师会被替换为艾克佐迪亚，

刻魔会被替换为刻印群魔的刻魔锻冶师。

**注意！** 请不要尝试设置两个相同的键，这是**未经测试**的行为，可能会导致**不预期的结果！**

## TODO
* 可配置的发送内容，能选择是否发送某一部分
* 仓库预置的卡片名称替换规则（期待issue能帮我想）
* `ck`命令支持更多参数，如显示第二第三搜索优先级的卡
* 更多的命令，如一次性可显示多张卡的命令、按字段搜索多张卡片的命令等
