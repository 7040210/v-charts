### 折线图

#### 示例

##### 普通折线图

<iframe width="100%" height="415"
src="https://jsfiddle.net/vue_echarts/bvtvvy0y/embedded/result,html,js/?bodyColor=fff" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

##### 折线图空值补零

- 此图中设置了空值补零，若不补零，则空值显示“－”

<iframe width="100%" height="415"
src="https://jsfiddle.net/vue_echarts/dx91mu73/2/embedded/result,html,js/?bodyColor=fff" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

##### 设置双y轴以及最大值最小值

- 双y轴折线图适用于数据大小相差较大或者数据类型不同时使用
- 是否脱离0值比例

<iframe width="100%" height="415" src="https://jsfiddle.net/vue_echarts/kxqh73jm/3/embedded/result,html,js/?bodyColor=fff" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

#### 面积图

<iframe width="100%" height="415" src="https://jsfiddle.net/vue_echarts/02jffyzu/embedded/result,html,js/?bodyColor=fff" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

#### 堆积图

　- 最好设置成为面积图否则很难看出堆积的效果

<iframe width="100%" height="415" src="https://jsfiddle.net/vue_echarts/eatvfLfr/embedded/result,html,js/?bodyColor=fff" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

#### 数据类型为percent时保留位数问题




#### settings 配置项

| 配置项 | 简介 | 类型 | 备注 |
| --- | --- | --- | --- |
| dimension | 维度 | Array | 默认columns第一项为维度 |
| metrics | 指标 | Array | 默认columns第二项为指标 |
| yAxisType | 左右坐标轴数据类型 | Array | 可选值: KMB, normal, percent |
| yAxisName | 左右坐标轴标题 | Array | - |
| axisSite | 指标所在的轴 | Object | 默认不在right轴的指标都在left轴 |
| stack | 堆叠选项 | Object | - |
| area | 是否展示为面积图 | Boolean | 默认为false |
| scale | 是否是脱离 0 值比例 | Array | 默认为[false, false]，表示左右<br>两个轴都不会脱离0值比例。<br>设置成 true 后坐标刻度不会<br>强制包含零刻度<br> |
| min | 左右坐标轴最小值 | Array | - |
| max | 左右坐标轴最大值 | Array | - |
| nullAddZero | 空值补零 | Boolean | 设置为true后，如果数据中对应某项<br>为null或undefined，则在表格中补0 |
| digit | 设置数据类型为percent时保留的位数 | Number | 默认为2 |

> 备注1. axisSite 可以设置 left 和 right，例如示例所示 `axisSite: { right: ['占比'] }` 即将占比的数据置于右轴上。

> 备注2. stack 用于将两数据堆叠起来，例如实例中所示`stack: { '销售额': ['销售额-1季度', '销售额-2季度'] }` 即将'销售额-1季度', '销售额-2季度'相应的数据堆叠在一起。

> 备注3. min和max的值可以直接设置为数字，例如：`[100, 300]`；也可以设置为`['dataMin', 'dataMin']`, `['dataMax', 'dataMax']`，此时表示使用该坐标轴上的最小值或最大值为最小或最大刻度。

