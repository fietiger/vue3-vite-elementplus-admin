<!--
 * @Description: 换肤
 * @Author: hutu
 * @Date: 2022-01-17 14:56:58
 * @LastEditors: hutu
 * @LastEditTime: 2022-01-17 15:40:59
-->
<template>
  <div class="theme">
    <div class="container">
      <SkinTheme />
    </div>
  </div>
</template>
<script lang="ts" setup>
import SkinTheme from '@/components/SkinTheme/Index.vue'
</script>
<style lang="scss" scoped>
.theme {
  overflow: auto;
  height: calc(100vh - 51px);
  .container {
    min-height: 500px;
    background: #fff;
    margin: 20px;
    padding: 20px;
    border-radius: 4px;
  }
}
</style>
