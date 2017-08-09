### 使用指南

#### 指标维度的解释

在阅读了图表相关的文档后，你会发现，图表数据的格式都是下面的这种形式：
```js
{
  columns: ['页面名', 'PV', 'UV'],
  rows: [
    { '页面名': '首页', 'PV': 10000, 'UV': 5000 },
    { '页面名': '餐厅详情页', 'PV': 8000, 'UV': 3000 },
    { '页面名': '下单页', 'PV': 5000, 'UV': 1000 }
  ]
}
```

将这种格式的数据使用表格的形式可以展示为如下所示

| 页面名 | PV | UV |
| -- | -- | -- |
| 首页 | 10000 | 5000 |
| 餐厅详情页 | 8000  | 3000 |
| 下单页 | 5000  | 1000 |

v-charts 的展示数据是由指标和维度来确定的

> “维度”是指数据的属性，例如 “页面名”维度表示用户浏览的页面名称<br>
“指标”是量化衡量标准，例如 “PV”和“UV”用来表示页面被浏览的次数

以折线图为例，折线图可以展示单维度多指标

<iframe width="100%" height="450" src="//jsfiddle.net/vue_echarts/39qs6zfk/1/embedded/result,html,js/?bodyColor=fff" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

饼图则只能展示单维度单指标

<iframe width="100%" height="450" src="//jsfiddle.net/vue_echarts/39qs6zfk/2/embedded/result,html,js/?bodyColor=fff" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

如果想用饼图展示多维度或者多指标，可以绘制多个饼图，或者是使用切换指标维度的方式实现

<iframe width="100%" height="450" src="//jsfiddle.net/vue_echarts/we718276/4/embedded/result,html,js/?bodyColor=fff" allowfullscreen="allowfullscreen" frameborder="0"></iframe>


