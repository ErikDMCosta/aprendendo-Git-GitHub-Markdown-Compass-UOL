<template>
  <div>
    <Header :esta_logado="true"/>
    <h1>Olá Mundo!</h1>
    <PrimeiroComponente />
    <p class="paragrafo-pai">O dado de app é: {{ testando }}</p>
    <life-cycle />
    <Info />
    <Pessoa />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'
import Info from './components/Info.vue'
  export default {
      name: 'App',
      components: {
        PrimeiroComponente,
        LifeCycle,
        Info,
        Header,
        Pessoa,
      },
      data() {
        return {
          testando: "teste"
        }
      }
    }
    
</script>

<style>
  body {
    background-color: #333;
    color: #FFF;
  }

  a {
    color: red;
  }

  .teste {
    background-color: #000;

  }

  .paragrafo-pai {
    color: red;

  }

</style>
