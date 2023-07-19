<template>
    <h1>Meu nome é: {{ name }}</h1>
</template>

<script>
    export default {
        name: "LifeCycle",
        data() {
            return {
                name: 'Ainda não sei'
            }
        },
        created(){
            this.name = "Guilherme"

            this.lifeCycle();
        },
        mounted() {
            this.name = "Pedro"
        },
        methods: {
            lifeCycle(){
                console.log('executou')
            }
        }
    }
</script>