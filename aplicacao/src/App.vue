<template>
  <h1>Olá mundo!</h1>
  <PrimeiroComponente />
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'

  export default {
    name: 'app',
    components: {
      PrimeiroComponente
    }
  }
</script>