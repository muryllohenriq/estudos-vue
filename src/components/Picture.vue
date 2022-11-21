<template>
  <div>
    <img :src="avatar" :alt="descricao" style="width: 10%"/>
    <Reutilizacao />
    <!-- ':' = 'v-bind:' -->
  </div>
</template>
<script>
import Reutilizacao from "./Reutilizacao.vue";

export default {
  name: "Picture",
  data() {
    return {
      avatar: "/img/profile-picture.jpg",
      descricao: "Muryllo Henrique",
    };
  },
  components: {
    Reutilizacao,
  },
};
</script>
