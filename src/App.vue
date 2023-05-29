<template>
  <el-config-provider namespace="ep" :locale="zhCn">
    <Parent />
  </el-config-provider>
</template>

<script setup lang="ts">
  import zhCn from 'element-plus/dist/locale/zh-cn.mjs'
</script>

<style>
#app {
  text-align: center;
}

.element-plus-logo {
  width: 50%;
}
</style>
