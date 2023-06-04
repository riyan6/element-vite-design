<template>
    <div>
        <div>
            <h2>1、关键词搜索</h2>
            <div style="width: 210px;">
                <el-input v-model="input1_1" placeholder="请输入查询内容">
                    <template #suffix>
                        <el-icon>
                            <Search />
                        </el-icon>
                    </template>
                </el-input>
                <p>搜索框默认状态</p>
            </div>
        </div>
        <div class="flex-column">
            <h2>2、输入框</h2>
            <div style="width: 320px;">
                <div class="flex">
                    <span style="width: 100px;">默认</span>
                    <el-input v-model="input2_1" placeholder="请输入" />
                </div>
            </div>
            <div style="width: 320px;">
                <div class="flex">
                    <span style="width: 100px;">已输入</span>
                    <el-input v-model="input2_2" placeholder="已输入" />
                </div>
            </div>
        </div>
        <div>
            <h2>3、文本域</h2>
            <div style="width: 210px;">
                <el-input v-model="input3_1" :rows="8" type="textarea" placeholder="Please input" />
                <p>搜索框默认状态</p>
            </div>
        </div>
    </div>
</template>


<script setup lang="ts">
import { ref } from 'vue';
import {
    Search
} from '@element-plus/icons-vue'


const input1_1 = ref('')
const input2_1 = ref('')
const input2_2 = ref('已输入')
const input3_1 = ref('已输入')

</script>

<style scoped>
.flex {
    display: flex;
    align-items: center;
}

.flex-column {
    display: flex;
    flex-direction: column;
    gap: 10px;
}
</style>