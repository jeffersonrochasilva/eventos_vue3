<template>
  <h1>app</h1>
  <p>{{ twoName }}</p>
  <p>{{ objeto.name }}</p>
  <p>{{ objeto.age }}</p>

  <Children
    :testando="testando"
    @emitir="send"
    @eventoDeSobreNome="twoName = $event"
  />
</template>
<script setup lang="ts">
import { Ref, ref } from "vue";
import Children from "@/components/Children.vue";
const twoName: Ref<string> = ref("");
const testando: Ref<string> = ref("testando");
const objeto: Ref<any> = ref({});

function send(data: any) {
  objeto.value = data;
  console.log(data);
}
function getLastName(res: any) {
  twoName.value = res;
}
</script>
<style>
#app {
  font-family: sans-serif;
  margin: 0;
  padding: 0;
}
</style>
