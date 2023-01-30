<template>
  <button @click="emitirEvento()">Send / Enviar</button>
</template>

<script setup lang="ts">
const emit = defineEmits(["emitir"]);

function emitirEvento() {
  emit("emitir", { nam: "Jefferson", age: 30 });
}
</script>
