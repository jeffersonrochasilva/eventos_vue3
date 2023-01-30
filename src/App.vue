<template>
  <h1>app</h1>
  <p>{{}}</p>
  <Children @emitir="send" />
</template>
<script setup lang="ts">
import Children from "@/components/Children.vue";

function send(data: any) {
  console.log(data);
}
</script>
<style>
#app {
  font-family: sans-serif;
  margin: 0;
  padding: 0;
}
</style>
