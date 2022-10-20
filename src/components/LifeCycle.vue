<template>
  <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>
export default {
  name: "LifeCycle",
  data() {
    return {
      nome: "Muryllo",
    };
  },
  created() {
    setTimeout(() => {
      this.nome = "Muryllinho";
    }, 1000);
  },
  mounted() {
    setTimeout(() => {
      this.nome = "Muryllao";
    }, 2000);
  },
};
</script>