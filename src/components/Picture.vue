<template>
  <div>
    <img :src="avatar" :alt="descricao" style="width: 10%" />
    <MudarImagem @mudar-imagem="sumirImagem" />
    <!-- ':' = 'v-bind:' -->
  </div>
</template>
<script>
import MudarImagem from "./MudarImagem.vue";

export default {
  name: "Picture",
  components: {
    MudarImagem,
  },
  data() {
    return {
      avatar: "/img/profile-picture.jpg",
      descricao: "Muryllo Henrique",
    };
  },
  methods: {
      sumirImagem() {
        this.avatar = ""
      }
  }
};
</script>
