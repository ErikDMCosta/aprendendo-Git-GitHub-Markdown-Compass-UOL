<template>
        <div>
                <img :src="avatar" :alt="descricao">
                <img :src="capa" :alt="descricao">
                <MudarImagem @mudar-imagem="trocarImagem" />
        </div>
</template>

<script>
    import Reutilizacao from './Reutilizacao.vue';
    import MudarImagem1 from './MudarImagem.vue';
    import MudarImagem2 from './MudarImagem.vue';

export default {
        name:'Picture', 
        components: {
              MudarImagem1,
              MudarImagem2
        },
        data() {
                return {
                        avatar: "/img/avatar.png",
                        capa: "/img/capa.png",
                        descricao: "Érik DM Costa"
                }
        },
        methods: {
                trocarImagem() {
                        //console.log("Opa");
                        this.avatar = "./img/avatar2.png";
                        this.capa = "./img/capa2.png";
                }
        }
}
</script>
<style scoped>
        img {
                width: 150px;
                height: 150px;
        }
</style>