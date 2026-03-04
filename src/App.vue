<script setup>
import { reactive, computed } from 'vue';
import Formulario from './components/Formulario.vue';
import Resultado from './components/Resultado.vue';

const estado = reactive({
  numeroA: '',
  numeroB: '',
  operacao: '+'
});

const resultado = computed(() => {
  const a = parseFloat(estado.numeroA);
  const b = parseFloat(estado.numeroB);

  if (isNaN(a) || isNaN(b)) return null;

  switch (estado.operacao) {
    case '+': return a + b;
    case '-': return a - b;
    case '*': return a * b;
    case '/': return b === 0 ? 'Erro: divisão por zero' : a / b;
  }
});
</script>

<template>
  <div class="container mt-5">
    <h1>Calculadora</h1>
    <Formulario
      :estado="estado"
      @atualiza="(campo, valor) => estado[campo] = valor"
    />
    <Resultado :resultado="resultado" />
  </div>
</template>
