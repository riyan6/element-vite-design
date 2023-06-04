<template>
    <div style="padding: 10px;">
        <el-tabs v-model="activeName" class="demo-tabs">
            <el-tab-pane label="Button 按钮" name="button">
                <ButtonPage />
            </el-tab-pane>
            <el-tab-pane label="Form 表单组件" name="form">
                <FormPage />
            </el-tab-pane>
        </el-tabs>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const activeName = ref('button')

</script>