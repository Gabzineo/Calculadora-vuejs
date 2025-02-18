<script setup>
import { reactive, computed } from 'vue';

const estado = reactive({
  primeirovalor: 0,
  segundovalor: 0,
  operacao: 'somar'
});

const resultado = computed(() => {
  const { primeirovalor, segundovalor, operacao } = estado;

  switch (operacao) {
    case 'somar':
      return primeirovalor + segundovalor;
    case 'subtrair':
      return primeirovalor - segundovalor;
    case 'multiplicar':
      return primeirovalor * segundovalor;
    case 'dividir':
      return segundovalor !== 0 ? (primeirovalor / segundovalor).toFixed(2) : 'Erro';
    default:
      return 0;
  }
});
</script>

<template>
  <div class="container bg-primary-subtle pb-4 pt-0 ps-0 pe-0">
    <header class="p-5 mt-5 mb-5 bg-primary text-white text-center rounded">
      <h1>Calculadora no Vue.js</h1>
      <p>Escolha a operação que deseja calcular</p>
    </header>
    
    <form>
      <div class="row justify-content-center">
        <div class="col-3">
          <input v-model.number="estado.primeirovalor" type="number" required placeholder="Digite o primeiro número" class="form-control">
        </div>
        <div class="col-3">
          <input v-model.number="estado.segundovalor" type="number" required placeholder="Digite o segundo número" class="form-control">
        </div>
        <div class="col-1">
          <select v-model="estado.operacao" class="form-control text-center">
            <option value="somar">+</option>
            <option value="subtrair">-</option>
            <option value="multiplicar">×</option>
            <option value="dividir">÷</option>
          </select>
        </div>
      </div>
      <div class="row justify-content-center m-4">
        <div class="col-3 text-center">
          <h1>Resultado: {{ resultado }}</h1>
        </div>
      </div>
    </form>
  </div>
</template>

<style scoped>
body {
  background-color: red;
}
</style>
