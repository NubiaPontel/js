<template>
  <div>
    <Header/>
    <PrimeiroComponente/>
    <p class="par-pai">O dado de App é {{ testando }}</p>
    <LifeCycle/>
    <Pessoa/>
  </div>
  
</template>


<script>
  import Header from './components/Header.vue'
  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import Pessoa from './components/Pessoa.vue'

  export default{
    name: 'App',
    components: {
      Header,
      PrimeiroComponente,
      LifeCycle,
      Pessoa
    },
    data(){
      return{
        testando: "Teste"
      }
    }
  }
</script>
<style>
  body{
    background-color: #333;
    color: #FFF;
  }
  a{
    color: red;
  }

  .teste{
    background-color: black;
  }

</style>