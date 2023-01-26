<template>
        <div>
                <img :src="avatar" :alt="descricao">
                <MudarImagem @mudar-imagem="trocarImagem" />
        </div>
</template>

<script>
    import Reutilizacao from './Reutilizacao.vue';
    import MudarImagem from './MudarImagem.vue';

export default {
        name:'Picture', 
        components: {
              MudarImagem
        },
        data() {
                return {
                        avatar: "/img/avatar.png",
                        descricao: "Érik DM Costa"
                }
        },
        methods: {
                trocarImagem() {
                        //console.log("Opa");
                        this.avatar = "./img/avatar2.png";
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