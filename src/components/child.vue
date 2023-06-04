<template>
    <h1>child</h1>
    <p>父组件传递的`<b>message</b>`值：<span style="color: red;">{{ message }}</span></p>
    <p><input :value="label" @input="inputTagValueChange" /></p>
    <p><ElButton type="primary" @click="onSendMessageToParent">发送消息给父组件</ElButton></p>
</template>

<script setup lang="ts">
import { ElMessage } from 'element-plus';
import { reactive, toRefs, defineExpose } from 'vue';

// prop
const prop = defineProps({
    message: { type: String, required: true },
    modelValue: {
        type: String,
        default: ''
    }
})
// emit
const emit = defineEmits(['update:modelValue', 'newMessage'])
// data
const state = reactive({
    label: prop.modelValue
})


// 抛出数据
const { label } = toRefs(state)


// 输入框事件
const inputTagValueChange = (event: any) => {
    const value = event.target.value
    state.label = value
    emit('update:modelValue', value)
}

// 发送消息给父组件
const onSendMessageToParent = () => {
    emit('newMessage',new Date().getTime())
}

// 供父组件调用的方法
const outFunc = () => {
    ElMessage.success('outFunc by child.vue')
}

defineExpose({ outFunc })

</script>

<style scoped lang="less"></style>