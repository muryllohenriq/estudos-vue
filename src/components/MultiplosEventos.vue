<template>
  <div>
    <button @click="primeiro('Primeiro evento', $event), segundo('Segundo evento', $event), terceiro()">Ativar múltiplos eventos</button>
    <p>{{multiplos_eventos}}</p>
  </div>
</template>
<script>
export default {
    name: 'MultiplosEventos',
    data() {
        return {
            multiplos_eventos: ''
        }
    },
    methods: {
        primeiro(txt, e) {
            this.multiplos_eventos = txt;
        },
        segundo(txt, e) {
            setTimeout(() => this.multiplos_eventos = txt, 500)
        },
        terceiro(txt, e) {
            setTimeout(() => this.multiplos_eventos = '', 1500)
        }
    }
};
</script>
<style scoped>
div {
  margin: 100px;
}
</style>