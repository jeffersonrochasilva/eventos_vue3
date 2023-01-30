<template>
  <button @click="emitirEvento()">Send / objeto</button>
  <button @click="emitirnovoEvento()">Send / sobre Nome</button>
  <h2>{{ props.testando }}</h2>
</template>

<script setup lang="ts">
import { Ref, ref } from "vue";
const nome: Ref<string> = ref("Jefferson");

const emit = defineEmits(["emitir", "eventoDeSobreNome"]);
const props = defineProps<{
  testando: String;
}>();

function emitirEvento() {
  emit("emitir", { name: "Jefferson", age: 30 });
}

function emitirnovoEvento() {
  emit("eventoDeSobreNome", nome.value);
}
</script>
