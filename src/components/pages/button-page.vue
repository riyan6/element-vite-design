<template>
    <div class="page">
        <el-row>
            <el-button>次要按钮</el-button>
            <el-button type="primary">主要按钮</el-button>
            <el-button type="success">成功按钮</el-button>
            <el-button type="warning">警告按钮</el-button>
            <el-button type="danger">危险按钮</el-button>
            <el-button type="info">信息按钮</el-button>
        </el-row>
        <el-row style="margin-top: 20px;">
            <el-button color="#e5e9fa" size="small">
                <el-icon>
                    <Search color="#526ade" />
                </el-icon>
            </el-button>
            <el-button type="primary" :icon="Plus" size="small" />
        </el-row>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import {
    Plus,
    Search,
} from '@element-plus/icons-vue'


const count = ref(0)

</script>

<style scoped>
.page {
    width: 100%;
}
</style>