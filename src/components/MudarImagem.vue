<template>
    <div>
        <button @click="$emit('mudarImagem')">Esconda meu rosto</button>
    </div>
</template>
<script>
export default {
    name: 'MudarImagem',
    emits: ['mudarImagem']
}
</script>