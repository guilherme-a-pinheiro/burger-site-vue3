<template>
    <div>
        <h1>Olá Vue!</h1>
        <p>Meu nome é: {{ name }} e trabalho como {{ profissao }}</p>
        <MultiplosEventos />
    </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos'

    export default {
        name: 'PrimeiroComponente',
        data() {
            return {
                name: 'Guilherme',
                profissao: 'Dev'
            }
        },
        components: {
            MultiplosEventos
        }
    }
</script>