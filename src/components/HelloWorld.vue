<script setup lang="ts">
import { ref } from "vue";
import { ElMessage } from "element-plus";

defineProps<{ msg: string }>();

const count = ref(0);
const input = ref("element-plus");
const choose = ref('')

const curDate = ref("");

const toast = () => {
  ElMessage.error("错了哦，这是一条错误消息");
};
</script>

<template>
  <h1>{{ msg }}</h1>

  <p>
    See
    <a href="https://element-plus.org" target="_blank">element-plus</a> for more
    information.
  </p>

  <!-- example components -->
  <div class="mb-4">
    <el-button size="large" @click="toast">El Message</el-button>
  </div>

  <div class="my-2 text-center flex flex-wrap justify-center items-center">
    <el-button @click="count++">count is: {{ count }}</el-button>
    <el-button type="primary" @click="count++">count is: {{ count }}</el-button>
    <el-button type="success" @click="count++">count is: {{ count }}</el-button>
    <el-button type="warning" @click="count++">count is: {{ count }}</el-button>
    <el-button type="danger" @click="count++">count is: {{ count }}</el-button>
    <el-button type="info" @click="count++">count is: {{ count }}</el-button>
  </div>

  <div>
    <el-tag class="m-1">primary</el-tag>
    <el-tag type="success" class="m-1">success</el-tag>
    <el-tag type="warning" class="m-1">warning</el-tag>
    <el-tag type="danger" class="m-1">danger</el-tag>
    <el-tag type="info" class="m-1">info</el-tag>
  </div>

  <div class="my-2">
    <el-input class="m-2" v-model="input" style="width: 200px" placeholder="请输入" />
    <el-date-picker class="m-2" v-model="curDate" type="date" placeholder="请选择"></el-date-picker>
    <el-select v-model="choose" placeholder="请选择">
      <el-option value="Arco" label="Arco" />
      <el-option value="Design" label="Design" />
    </el-select>
  </div>

  <div style="display: flex; justify-content: center;">
    <el-card style="width: 500px;">
      <h1>el-card</h1>
      <h1>el-card</h1>
      <h1>el-card</h1>
    </el-card>
  </div>


  <p>For example, we can custom primary color to 'green'.</p>

  <p>
    Edit
    <code>components/HelloWorld.vue</code> to test components.
  </p>
  <p>
    Edit
    <code>styles/element/var.scss</code> to test scss variables.
  </p>

  <p>
    Full Example:
    <a href="https://github.com/element-plus/element-plus-vite-starter" target="_blank">element-plus-vite-starter</a>
    | On demand Example:
    <a href="https://github.com/element-plus/unplugin-element-plus"
      target="_blank">unplugin-element-plus/examples/vite</a>
  </p>
</template>

<style>
.ep-button {
  margin: 4px;
}

.ep-button+.ep-button {
  margin-left: 0;
  margin: 4px;
}
</style>
