<!--
 * @Description: 柱状图
 * @Author: hutu
 * @Date: 2022-01-06 14:51:10
 * @LastEditors: hutu
 * @LastEditTime: 2022-01-17 14:27:46
-->
<template>
  <div class="bar">
    <EchartInit id="bar" width="100%" height="100%" :option="state.option" />
  </div>
</template>
<script lang="ts" setup>
import * as echarts from 'echarts/core'
import EchartInit from '@/components/EchartInit/Index.vue'
import { IEchartsOption } from '@/interface'
import { reactive } from 'vue'
const state = reactive({
  option: {
    grid: {},
    tooltip: {
      trigger: 'axis',
      axisPointer: {
        type: 'shadow'
      }
    },
    xAxis: {
      type: 'category',
      data: ['1月3日', '1月4日', '1月5日', '1月6日', '1月7日', '1月8日', '1月9日']
    },
    yAxis: {
      type: 'value'
    },
    series: [
      {
        data: [3, 5, 3, 0.4, 1, 0.5, 0.9],
        type: 'bar',
        showBackground: true,
        backgroundStyle: {
          color: 'rgba(180, 180, 180, 0.2)'
        },
        itemStyle: {
          normal: {
            color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [
              {
                offset: 0,
                color: '#cee0f7'
              },
              {
                offset: 0.7,
                color: '#62a5f7'
              },
              {
                offset: 1,
                color: '#3a8df3'
              }
            ])
          }
        }
      }
    ]
  } as IEchartsOption
})
</script>

<style lang="scss" scoped>
.bar {
  height: 100%;
}
</style>
