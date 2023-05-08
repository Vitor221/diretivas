<template>
  <div>
    <p v-texto="{ cor: 'red', tamanhoFonte: '200%', totalCaracteres: 15 }">Primeira diretiva customizada</p>
    <p v-texto="configuracaoTexto">Teste</p>

    <div v-posicao:absolute="80" v-texto="{ cor: 'green', tamanhoFonte: '200%', totalCaracteres: 100}">
      Olá, eu sou um binding de argumento e valor
    </div>

    <span>Código A</span><input type="text"><span v-informacao:simples.umClickMouse.sairAutomaticamente="'Você encontrará o código A na parte frontal do equipamento'"> i</span>
    <br>
    <span>Código A</span><input type="text"><span v-informacao:destacado.doisClickMouse.sairAutomaticamente="'Você encontrará o código B na parte traseira do equipamento, abaixo da tampa de proteção'"> i</span>

    <hr>

    <h1 v-colorir="'brown'">Diretiva customizada registrada localmente (no componente)</h1>
  </div>
</template>

<script>
import colorirFundoTexto from '@/directives/colorirFundoTexto'

export default {
  name: 'App',
  directives: {
    colorir: colorirFundoTexto
  },
  data: () => ({
    configuracaoTexto: { cor: 'blue', tamanhoFonte: '300%', totalCaracteres: 4}
  })
}
</script>

<style>

</style>
