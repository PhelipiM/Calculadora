<script>

function calcular(){
  let totalConta = document.getElementyById("valorConta").value;
  let gorjeta = document.getElementById("gorjeta").value;
  let pessoas = document.getElementById("numPessoas").value;
}

document.getElementById("salvar").onclick = function(){
  calcular();
}


</script>

<template>
  <div id="main" data-v-app="">
    <h1 selecoes="">Calculadora de Gorjetas</h1>
    <form action="" class="tipForm" selecoes="">
      <label for="valorConta" selecoes="">Qual o valor da conta?</label>
        <input name="valorConta" type="number" selecoes="">
      <label for="percentageService" selecoes="">Como foi o serviço?</label>
      <select selecoes="" id="gorjeta">
        <option value="30" selecoes="">30% (Excepcional)</option>
        <option value="25" selecoes="">25% (Mais do que bom)</option>
        <option value="20" selecoes="">20% (Bom)</option>
        <option value="15" selecoes="">15% (OK)</option>
        <option value="10" selecoes="">10% (Ruim)</option>
        <option value="5" selecoes="">5% (Péssimo)</option>
      </select>
      <label for="qtyPeople" selecoes="">Quantas pessoas estão pagando a conta?</label>
      <input name="qtyPeople" type="number" selecoes="" id="numPessoas">
    </form>
    <div class="result" selecoes=""> Valor da conta:
      <span class="billValuePerPerson" selecoes="">R$ 0.00 por pessoa</span>
    </div>
    <div class="calculo" selecoes="">
      <button id="salvar"> Calcular </button>
    </div>
  </div>
</template>