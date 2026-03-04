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
  <div class="page">
    <div class="card">
      <div class="card-header">
        <div class="icon">🧮</div>
        <h1>Calculadora</h1>
        <p>Preencha os campos e veja o resultado em tempo real</p>
      </div>

      <Formulario
        :estado="estado"
        @atualiza="(campo, valor) => estado[campo] = valor"
      />

      <Resultado :resultado="resultado" />
    </div>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
}

.page {
  min-height: 100vh;
  background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
}

.card {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 24px;
  padding: 40px;
  width: 100%;
  max-width: 520px;
  box-shadow: 0 25px 50px rgba(0, 0, 0, 0.4);
}

.card-header {
  text-align: center;
  margin-bottom: 36px;
}

.card-header .icon {
  font-size: 48px;
  margin-bottom: 12px;
}

.card-header h1 {
  font-size: 28px;
  font-weight: 700;
  color: #ffffff;
  margin-bottom: 6px;
}

.card-header p {
  font-size: 13px;
  color: rgba(255, 255, 255, 0.45);
  font-weight: 300;
}
</style>
