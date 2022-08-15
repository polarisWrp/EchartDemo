<template>
  <h1>{{ msg }}</h1>
  <div id="idK">这是dog</div>
</template>

<script setup lang="ts">
import { ref, onBeforeMount, onMounted, onBeforeUpdate, onUpdated,onBeforeUnmount, onUnmounted } from 'vue'
// 首先是执行 setup
console.log('setup');
let msg = ref('')
onBeforeMount(() => {
const item = document.querySelector('#idK')
// dom挂载之前获取dom元素失败  null 
  console.log('这是item', item);
})
onMounted(() => {
  const item = document.querySelector('#idK')
  console.log('挂载完了、、',item);
})
// 接着是 更新前，更新完成，卸载前，卸载后

</script>

<style scoped>

</style>
