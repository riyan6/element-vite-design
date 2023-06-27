<template>
  <div class="table-component">
    <el-table class="table" :data="tableData">
      <el-table-column prop="date" label="Date" width="180" />
      <el-table-column prop="name" label="Name" width="180" />
      <el-table-column prop="address" label="Address" />
    </el-table>
    <div class="pagination-area">
        <el-pagination background layout="total, prev, pager, next" :total="50" />
    </div>
  </div>
</template>

<script setup lang="ts">
const tableData = [
  {
    date: "2016-05-03",
    name: "Tom",
    address: "No. 189, Grove St, Los Angeles",
  },
  {
    date: "2016-05-02",
    name: "Tom",
    address: "No. 189, Grove St, Los Angeles",
  },
  {
    date: "2016-05-04",
    name: "Tom",
    address: "No. 189, Grove St, Los Angeles",
  },
  {
    date: "2016-05-01",
    name: "Tom",
    address: "No. 189, Grove St, Los Angeles",
  },
];
</script>

<style scoped>
.table-component {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
}
.table {
    flex: 1;
}
.pagination-area {
    padding: 10px;
}
</style>
