<script setup>
const props = defineProps(['estado']);
const emit = defineEmits(['atualiza']);
</script>

<template>
  <div class="row mt-4">
    <div class="col">
      <label>Número A</label>
      <input
        :value="props.estado.numeroA"
        @input="evento => emit('atualiza', 'numeroA', evento.target.value)"
        type="number"
        class="form-control"
        placeholder="Digite o número A"
      />
    </div>

    <div class="col-md-3">
      <label>Operação</label>
      <select
        :value="props.estado.operacao"
        @change="evento => emit('atualiza', 'operacao', evento.target.value)"
        class="form-control"
      >
        <option value="+">+ Adição</option>
        <option value="-">- Subtração</option>
        <option value="*">× Multiplicação</option>
        <option value="/">÷ Divisão</option>
      </select>
    </div>

    <div class="col">
      <label>Número B</label>
      <input
        :value="props.estado.numeroB"
        @input="evento => emit('atualiza', 'numeroB', evento.target.value)"
        type="number"
        class="form-control"
        placeholder="Digite o número B"
      />
    </div>
  </div>
</template>
