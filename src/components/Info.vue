<template>
        <div>
                <p>{{ compEmail }} {{ email }}</p>
                <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
                <p v-else>Estou em busca de novas possibilidades</p>
                <p>Utilizo as seguintes tecnologias para Back-End: </p>
                <ul>
                        <li v-for="(technology, index) in backend_technologies" v-bind:key="index">
                                {{ technology }}

                        </li>
                </ul>
                <p>Utilizo as seguintes tecnologias para Front-End: </p>
                <ul>
                        <li v-for="technology in frontend_technologies" :key="technology.id">
                                {{ technology.language }}
                        </li>
                </ul>
                <div>
                        <button @click="showEmail">{{ textoBotao }}</button>
                </div>
                <p v-if="1 > 2">Testando</p>
                <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
                <p class="teste">Para acessar meu portfólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
                <Picture />
        </div>
</template>

<script>

import Picture from './Picture.vue'

export default {
        name: 'Info',
        components: {
                Picture
        },
        props: {
                email: String,
                esta_trabalhando: Boolean
        },
        data() {
                return { 
                        esta_trabalhando: false,
                        mostrar_email: false,
                        meu_link: 'https://google.com',
                        textoBotao: 'Mostrar e-mail',
                        backend_technologies: ['JavaScript', 'PHP', 'Python'],
                        frontend_technologies: [
                                {id: 1, language: 'HTML'},
                                {id: 2, language: 'CSS'},
                                {id: 3, language: 'VUE'}
                        ]
                }
        },
        methods: {
                showEmail() {
                        // console.log("Testando Método");
                        this.mostrar_email = !this.mostrar_email;
                        if (!mostrar_email) {
                                this.textoBotao = "Mostrar e-mail";
                        } else {
                                this.textoBotao = "Esconder e-mail";
                        }
                }
        }
}

</script>
