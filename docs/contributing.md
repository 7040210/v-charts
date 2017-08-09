### CONTRIBUT GUIDE

#### 关于属性

1. v-charts 是基于指标（metrics）和维度（dimension）来配置数据展示内容（参考使用指南），
所以在 setting 中应提供指标维度的配置项，用于用户选择数据中哪些为指标，哪些为维度。

2. 为了统一图表处理关于数据格式的问题，settings中应提供关于数据格式的配置项。

3. v-charts 图表配置项处理模块应专注于处理 `xAxis`、 `yAxis`、 `tooltip`、 `series`、
 `legend` 等与数据转换直接相关的部分，相应的属性置于settings中，例如：`dataType`；
 而类似 `grid`、 `dataZoom`、`visualMap`、`toolbox`等配置，无需参与数据转化而只需
 根据转化后的数据即可设置的配置项，应尽量直接放在组件上。

4. 图表的处理应尽量满足能够方便的处理[echarts文档](http://echarts.baidu.com/option.html)
中对应项的配置，例如`itemStyle, label`等。
