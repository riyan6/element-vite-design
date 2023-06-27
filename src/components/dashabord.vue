<template>
    <div class="dashbaord-page">
        <Table />
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const activeName = ref('button')

</script>

<style>
.dashbaord-page {
    width: 100vw;
    height: 100vh;
}
</style>