<template>
  <el-config-provider namespace="ep" :locale="zhCn">
    <BaseHeader />
    <div style="display: flex">
      <BaseSide />
      <div>
        <img alt="Vue logo" class="element-plus-logo" src="./assets/logo.png" />
        <HelloWorld msg="Hello Vue 3.0 + Element Plus + Vite" />
      </div>
    </div>
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
