<template>
  <div>
    <Header />
    <h1>Olá mundo!</h1>
    <PrimeiroComponente />
    <LifeCycle />
    <Pessoa />
    <Form />
  </div>
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue';
import Pessoa from './components/Pessoa.vue';
import Form from './components/Form.vue';
import Header from './components/Header.vue'

  export default {
    name: 'app',
    components: {
      PrimeiroComponente,
      LifeCycle,
      Pessoa,
      Form,
      Header
    }
  }
</script>

<style>
  body {
    background-color: #333;
    color: #fff;
  }

  a {
    color: red;
  }
</style>