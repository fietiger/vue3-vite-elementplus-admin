<template>
  <div class="dashboard">
    <PanelGroup :list="state.panelList" />
    <el-row>
      <el-col :xs="24" :sm="24" :lg="24">
        <LineChart />
      </el-col>
    </el-row>
    <el-row :gutter="25" style="margin-bottom: 20px">
      <el-col :xs="24" :sm="24" :lg="8">
        <div class="chart-wrapper">
          <BarChart />
        </div>
      </el-col>
      <el-col :xs="24" :sm="24" :lg="8">
        <div class="chart-wrapper">
          <PieChart />
        </div>
      </el-col>
      <el-col :xs="24" :sm="24" :lg="8">
        <div class="chart-wrapper">
          <TestChart />
        </div>
      </el-col>
    </el-row>
  </div>
</template>
<script lang="ts" setup>
import TestChart from './components/TestChart.vue'
import LineChart from './components/LineChart.vue'
import BarChart from './components/BarChart.vue'
import PieChart from './components/PieChart.vue'
import PanelGroup from './components/PanelGroup.vue'
import { reactive } from 'vue'
const state = reactive({
  panelList: [
    { icon: 'icon-adduser', num: 14, title: '注册用户', percent: 0.1201, bg: '#27C24C' },
    { icon: 'icon-team', num: 327, title: '访客数', percent: 0.0201, bg: '#F05050' },
    { icon: 'icon-barchart', num: 616, title: '访问量', percent: 0.135, bg: '#7266ba' },
    { icon: 'icon-ip', num: 515, title: '访问IP数', percent: -0.0103, bg: '#23b7e5' },
    { icon: 'icon-guanliyuan', num: 2, title: '管理员', percent: 0.0, bg: '#27C24C' },
    { icon: 'icon-reloadtime', num: 94.93, title: '浏览时长', percent: 0.3301, bg: '#F05050' },
    { icon: 'icon-file-text-fill', num: 14, title: '文章数', percent: 0.0, bg: '#7266ba' },
    { icon: 'icon-eye-fill', num: 2522, title: '阅读量', percent: 0.031, bg: '#23b7e5' }
  ]
})
</script>
<style lang="scss">
.dashboard {
  overflow-y: auto;
  overflow-x: hidden;
  height: 100%;
  padding: 0 20px;
  .chart-wrapper {
    margin: 20px 0 0;
  }
}
</style>
