<template>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades</p>
    <p>Utilizo as seguintes tecnologias:</p>
    <ul>
        <li>TS</li>
        <li>React</li>
        <li>Vue</li>
    </ul>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <p v-if="3 > 2">Testando</p>
</template>
<script>
export default {
    name: 'info',
    data() {
        return {
            esta_trabalhando: false,
            mostrar_email: true,
            email: 'muryllo@email.com'
        }
    }
}
</script>