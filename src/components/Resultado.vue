<script setup>
const props = defineProps(['resultado']);
</script>

<template>
  <div class="resultado" :class="{ ativo: props.resultado !== null, erro: typeof props.resultado === 'string' }">
    <span class="label">Resultado</span>
    <span class="valor">
      {{ props.resultado !== null ? props.resultado : '—' }}
    </span>
  </div>
</template>

<style scoped>
.resultado {
  background: rgba(255, 255, 255, 0.04);
  border: 1px dashed rgba(255, 255, 255, 0.12);
  border-radius: 16px;
  padding: 24px 28px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  transition: all 0.3s ease;
}

.resultado.ativo {
  background: rgba(108, 99, 255, 0.15);
  border: 1px solid rgba(108, 99, 255, 0.4);
  box-shadow: 0 0 24px rgba(108, 99, 255, 0.15);
}

.resultado.erro {
  background: rgba(255, 80, 80, 0.1);
  border-color: rgba(255, 80, 80, 0.4);
}

.label {
  font-size: 12px;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: rgba(255, 255, 255, 0.35);
}

.valor {
  font-size: 32px;
  font-weight: 700;
  color: #ffffff;
  transition: color 0.3s;
}

.resultado.ativo .valor {
  color: #a89cff;
}

.resultado.erro .valor {
  color: #ff6b6b;
  font-size: 14px;
  font-weight: 500;
}
</style>
