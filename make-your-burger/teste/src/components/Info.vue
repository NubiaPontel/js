<template>
    <div>
        <p>{{ compEmail }}</p>
        <p v-if="esta_trabalhando">Estou estudando no momento</p>
        <p v-else>Estou em busca de novas oportunidades</p>
        <p>Utilizo as seguintes tecnologias para backend:</p>
        <ul>
            <li v-for="(technology, index) in backend_technologies" v-bind:key="index">
                {{ technology }}
            </li>    
        </ul>
        <p>Utilizo as seguintes tecnologias para frontend:</p>
        <ul>
            <li v-for="technology in frontend_technologies" :key="technology.id">
                {{ technology.language }}
            </li>
        </ul>
        <div>
            <button @click="showEmail">Mostrar email</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p class="teste">Para acessar meu portifólio <a v-bind:href="link" target="_blanck">basta clicar aqui</a></p>
    </div>
</template>

<script>
export default{
    name: 'Info',
    props: {
        email: String 

    },
    data(){
        return{
            esta_trabalhando: false,
            mostrar_email: false,
            link: "https://google.com",
            backend_technologies: ['JavaScript', 'Python', 'C'],
            frontend_technologies:[
                {id: 1, language: 'HTML'},
                {id: 2, language: 'CSS'},
                {id: 3, language: 'VUE'}
            ]
        }
    },
    methods:  {
        showEmail(){
            this.mostrar_email = !this.mostrar_email
        }
    }
}
</script>

<style>
    .par-pai{
        color: red;
    }
</style>
