# native-echarts

## install

$ npm install native-echarts --save

## Usage

###用法

用法完全和echarts一致，将echarts的option传给组件。option详细属性详见[文档](http://echarts.baidu.com/option.html#title)

native-echarts共暴露了三个属性:

* *option* (object): echarts图表的配置项，无默认值。 
* *width* (number): 图表的宽度，默认值为其外层容器的宽度。 
* *height* (number): 图表的高度，默认值为400。 


```js
import React, { Component } from 'react';
import {
  AppRegistry,
  StyleSheet,
  Text,
  View
} from 'react-native';
import Echarts from 'native-echarts';

export default class app extends Component {
  render() {
    const option = {
      title: {
          text: 'ECharts 入门示例'
      },
      tooltip: {},
      legend: {
          data:['销量']
      },
      xAxis: {
          data: ["衬衫","羊毛衫","雪纺衫","裤子","高跟鞋","袜子"]
      },
      yAxis: {},
      series: [{
          name: '销量',
          type: 'bar',
          data: [5, 20, 36, 10, 10, 20]
      }]
    };
    return (
      <Echarts option={option} height={300} />
    );
  }
}

AppRegistry.registerComponent('app', () => app);

```



