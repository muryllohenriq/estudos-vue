<template>
  <img :src="avatar" :alt="descricao" />
  <!-- ':' = 'v-bind:' -->
</template>
<script>
export default {
  name: "Picture",
  data() {
    return {
      avatar: "/img/profile-picture.jpg",
      descricao: "Muryllo Henrique",
    };
  },
};
</script>
