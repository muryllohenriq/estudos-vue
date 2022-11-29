<template>
  <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
  <p v-else>Estou em busca de novas oportunidades</p>
  <p>Utilizo as seguintes tecnologias para back-end:</p>
  <ul>
    <li v-for="(technology, index) in backend_technologies" v-bind:key="index">
      {{ technology }}
    </li>
  </ul>
  <p>Utilizo as seguintes tecnologias para front-end:</p>
  <ul>
    <li v-for="technology in frontend_technologies" :key="technology.id">
      {{ technology.language }}
    </li>
  </ul>
  <div>
    <button @click="showEmail">{{ textoBotao }}</button>
  </div>
  <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
  <p class="teste">
    Para acessar meu portfólio
    <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a>
  </p>
  <Picture />
  <p v-if="3 > 2">Testando</p>
</template>
<script>
import Picture from "./Picture.vue";

export default {
  name: "info",
  components: {
    Picture,
  },
  props: {
    email: String,
    esta_trabalhando: Boolean
  },
  data() {
    return {
      mostrar_email: false,
      meu_link: "https://github.com/muryllohenriq",
      textoBotao: "Mostrar e-mail",
      backend_technologies: ["javascript", "node", "express", "mysql"],
      frontend_technologies: [
        { id: 1, language: "CSS" },
        { id: 2, language: "React" },
        { id: 3, language: "TypeScript" },
      ],
    };
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email; // quando clicar ele virará o oposto
      if (!this.mostrar_email) {
        this.textoBotao = "Mostrar e-mail";
      } else {
        this.textoBotao = "Esconder e-mail";
      }
    },
  },
};
</script>

<style>
.paragrafo-pai {
  color: #999;
}
</style>