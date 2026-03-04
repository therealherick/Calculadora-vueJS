<script setup>
const props = defineProps(['resultado']);
</script>

<template>
  <div class="mt-4 p-3 bg-light rounded">
    <h4 v-if="props.resultado === null">Preencha os campos acima</h4>
    <h4 v-else>Resultado: {{ props.resultado }}</h4>
  </div>
</template>
