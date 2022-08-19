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
    const valorConta = this.valorConta;
    const Gorjeta = this.Gorjeta;
    const numPessoas = this.numPessoas;
    let valorGorjeta = 0;
    let valorTotal= {};

    valorGorjeta = valorConta * (Gorjeta / 100);
    valorTotal = (valorConta + valorGorjeta) / numPessoas;

    console.log(valorTotal);

    document.getElementById("resultado").innerHTML = valorTotal;

  }
 }
};


</script>

<template>
  <div id="main">
    <form>

      <label>
        <p>Qual o preço do jantar?</p>
        <input type="number" v-model="valorConta" id="valorConta">
      </label>

      <label>
        <p>Qual a gorjeta?</p>
        <select v-model="Gorjeta" id="valorGorjeta">
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
        <input v-model="numPessoas" type="number" id="numPessoas">
      </label>

      <label>
        <button type="button" @click="calcular">Calcular</button>
      </label>

      <label>
        R$:<span id="resultado"> 0.00 </span>
      </label>

    </form>
  </div>
</template>