<script setup>
const props = defineProps(['estado']);
const emit = defineEmits(['atualiza']);
</script>

<template>
  <div class="formulario">
    <div class="campos">
      <div class="campo">
        <label>Número A</label>
        <input
          :value="props.estado.numeroA"
          @input="evento => emit('atualiza', 'numeroA', evento.target.value)"
          type="number"
          placeholder="0"
        />
      </div>

      <div class="campo campo-operacao">
        <label>Operação</label>
        <select
          :value="props.estado.operacao"
          @change="evento => emit('atualiza', 'operacao', evento.target.value)"
        >
          <option value="+">+</option>
          <option value="-">−</option>
          <option value="*">×</option>
          <option value="/">÷</option>
        </select>
      </div>

      <div class="campo">
        <label>Número B</label>
        <input
          :value="props.estado.numeroB"
          @input="evento => emit('atualiza', 'numeroB', evento.target.value)"
          type="number"
          placeholder="0"
        />
      </div>
    </div>
  </div>
</template>

<style scoped>
.formulario {
  margin-bottom: 28px;
}

.campos {
  display: flex;
  gap: 12px;
  align-items: flex-end;
}

.campo {
  display: flex;
  flex-direction: column;
  gap: 8px;
  flex: 1;
}

.campo-operacao {
  flex: 0 0 72px;
}

label {
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: rgba(255, 255, 255, 0.4);
}

input,
select {
  background: rgba(255, 255, 255, 0.07);
  border: 1px solid rgba(255, 255, 255, 0.12);
  border-radius: 12px;
  color: #ffffff;
  font-family: 'Poppins', sans-serif;
  font-size: 18px;
  font-weight: 500;
  padding: 14px 16px;
  outline: none;
  transition: border-color 0.2s, background 0.2s;
  width: 100%;
  -webkit-appearance: none;
  appearance: none;
  text-align: center;
}

input::placeholder {
  color: rgba(255, 255, 255, 0.2);
}

input:focus,
select:focus {
  border-color: #6c63ff;
  background: rgba(108, 99, 255, 0.1);
}

select {
  cursor: pointer;
  font-size: 22px;
}

select option {
  background: #1a1a2e;
}

input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
}

input[type="number"] {
  -moz-appearance: textfield;
}
</style>
