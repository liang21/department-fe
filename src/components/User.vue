<template>
  <div class="card">
    <h1>用户:{{ user }}</h1>
    <div>
      <el-button type="primary" v-if="isActive1" @click="changeButton()"
        >开始</el-button
      >
      <el-button type="danger" v-if="isActive2" @click="changeButton()"
        >结束</el-button
      >
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
const user = ref("张三");
const isActive1 = ref(true);
const isActive2 = ref(false);
const changeButton = () => {
  isActive1.value = !isActive1.value;
  isActive2.value = !isActive2.value;
};
</script>

<style scoped></style>
