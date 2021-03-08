<template>
  <Main />
</template>

<script setup>
import Main from './views/main.vue'
import { onMounted } from "vue";
const importStyle = () => import("./assets/style.less")

onMounted(async () => {
  const style = (await importStyle()).default;
  console.log(style);
});
</script>

<style>
#app {}
</style>