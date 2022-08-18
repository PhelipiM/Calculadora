<script>
export default {
 data(){
  return {
    valorConta: 0,
    Gorjeta: 0,
    numPessoas: 1,
  };
 },
 methods: {
  calcular(){
    valorGorjeta = valorConta * (Gorjeta / valorConta);
    valorTotal = (valorConta + valorGorjeta) / numPessoas;
  }
 }
};


</script>

<template>
  <div id="main">
    <form>

      <label>
        <p>Qual o preço do jantar?</p>
        <input type="number" id="valorConta">
      </label>

      <label>
        <p>Qual a gorjeta?</p>
        <select id="valorGorjeta">
          <option selected value="30">30% Ótimo serviço</option>
          <option value="25">25% Ótimo serviço</option>
          <option value="20">20% Ótimo serviço</option>
          <option value="15">15% Ótimo serviço</option>
          <option value="10">10% Ótimo serviço</option>
          <option value="5">5% Ótimo serviço</option>
        </select>
      </label>

      <label>
        <p>Quantas pessoas vão dividir a conta?</p>
        <input type="number" id="numPessoas">
      </label>

      <label>
        <button type="button" @click="calcularJantar">Calcular</button>
      </label>

      <label >
        <span id="resultado">0.00</span>
      </label>

    </form>
  </div>
</template>