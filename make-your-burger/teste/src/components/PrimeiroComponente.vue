<template>
    <div>
        <h1>Ola Vue</h1>
        <p>Meu nome é {{ nome }} e trabalho como {{ profissão }}</p>
        <MultiplosEventos/>
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
    </div>
</template>

<script>

    import MultiplosEventos from './MultiplosEventos'
    import Reutilizacao from "./Reutilizacao.vue";

    export default {
        name: 'PrimeiroComponente',
        components: {
            MultiplosEventos,
            Reutilizacao
        },
        data(){
            return{
                nome: "Nubia",
                profissão: "Programadora Vue"
            }
        }
    }

</script>
