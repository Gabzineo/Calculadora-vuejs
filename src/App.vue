<script setup>


</script>

<template>
  
  <div class="container bg-primary-subtle pb-4 pt-0 ps-0 pe-0">
  <header class="p-5 mt-5 mb-5 bg-primary text-white text-center rounded" >
    <h1>Calculadora no Vue.Js</h1>
    <p>Escolha a operação que deseja multiplicar</p>
  </header>
  <form >
    <div class="row justify-content-center">
      <div class="col-3">
        <input type="text" required placeholder="Digite o primeiro numero" class="form-control">
      </div>
      <div class="col-3">
        <input type="text" required placeholder="Digite o segundo numero" class="form-control">
      </div>
      <div class="col-1 ">
        <select class="form-control text-center">
          <option value="somar">+</option>
          <option value="subtrair">-</option>
          <option value="multiplicar">x</option>
          <option value="dividir">÷</option>
        </select>
      </div>
      </div>
      <div class="row justify-content-center m-4">
        <div class="col-3 text-center">
          <h1>Resposta</h1>
        </div>
      </div>
  </form>
</div>

  

</template>

<style scoped>
body{
  background-color: red;
}

</style>
