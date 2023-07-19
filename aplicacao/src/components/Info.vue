<template>
    <div>
        <p>{{compEmail}} - {{ email }}</p>
        <p v-if="esta_trabalhando">Estou trabalho no momento.</p>
        <p v-else>Estou em busca de novas oportunidades</p>
        <p>Utilizo as seguintes tecnologias para backend:</p>
        <ul>
            <li v-for="(technology, index) in backend_tecnologies" v-bind:key="index">{{ technology }}</li>
        </ul>

        <p>Utilizo as seguintes tecnologias para frontend:</p>
        <ul>
            <li v-for="technology in frontend_tecnologies" :key="technology.id">{{ technology.language }}</li>
        </ul>
        <div>
            <button @click="showEmail">{{ textoBotao }}</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p>Para acessar meu portifólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
    </div>
</template>

<script>
    export default {
        name: 'Info',
        props: {
            email: String,
            esta_trabalhando: Boolean
        },
        data() {
            return {
                mostrar_email: false,
                meu_link: 'https://google.com',
                textoBotao: 'Mostrar e-mail',
                backend_tecnologies: ['JavaScript', 'PHP', 'Python', 'Java'],
                frontend_tecnologies: [
                    {id: 1, language: 'HTML'},
                    {id: 2, language: 'CSS'},
                    {id: 3, language: 'Vue'}
            ]
            }
        },
        methods: {
            showEmail() {
                this.mostrar_email = !this.mostrar_email
                if (this.mostrar_email) {
                    this.textoBotao = 'Esconder e-mail'
                }
                else {
                    this.textoBotao = 'Mostrar e-mail'
                }
            }
        }
    }
</script>