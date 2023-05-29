<template>
    <!-- 父元素 -->
    <h1>parent</h1>
    <p>属性列表</p>
    <p>
        <ElTag>message</ElTag> {{ message }}
    </p>
    <p>
        <ElTag>computed message</ElTag> {{ realMessage }}
    </p>
    <p>
        <ElTag>computed message2</ElTag> {{ realMessage2 }}
    </p>
    <p>
        <ElTag>computed realStatus</ElTag> {{ realStatus }}
    </p>
    <p>
        <ElTag>status</ElTag> {{ status }}
    </p>
    <p>
        <ElTag>修改次数</ElTag> {{ updateCount }}
    </p>
    <p>
        <ElInput v-model="message" style="width: 210px;" />
    </p>
    <ElDivider />
    <p>子消息传递列表：{{ childMessageList }}</p>
    <ElDivider />
    <!-- 子组件 -->
    <child :message="message" v-model="status" @new-message="reviceNewMessage" />
</template>

<script setup lang="ts">
import { computed, reactive, toRefs, watch } from 'vue';

// data
const state = reactive({
    message: '处理成功',
    status: 'health',
    childMessageList: [] as any[],
    updateCount: 0
})

// computed
const realMessage = computed(() => `【${state.message}】`)
const realMessage2 = computed(() => {
    return "新消息：" + state.message
})

// 抛出数据
const { message, childMessageList, status, updateCount } = toRefs(state)

// 监听
watch(message, (newVal, oldVal) => {
    console.log(`message发生了改变,新值：${newVal} 旧值：${oldVal}`)
})


// 子组件通信
const reviceNewMessage = (val: any) => {
    state.childMessageList.push(val)
}

</script>

<style scoped lang="less"></style>