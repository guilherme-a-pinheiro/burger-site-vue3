<template>
    <div>
        <h2>Essa é a descrição da pessoa: {{ name }}</h2>
        <Info />
    </div>
</template>


<script>
    import Info from './Info'

    export default {
        name: 'Pessoa',
        components: {
            Info
        },
        data() {
            return {
                name: 'Guilherme'
            }
        }
    }
</script>