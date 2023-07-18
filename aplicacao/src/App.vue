<template>
  <h1>Olá mundo!</h1>
  <PrimeiroComponente />
  <LifeCycle />
  <Pessoa />
  <Form />
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue';
import Pessoa from './components/Pessoa.vue';
import Form from './components/Form.vue';

  export default {
    name: 'app',
    components: {
      PrimeiroComponente,
      LifeCycle,
      Pessoa,
      Form
    }
  }
</script>