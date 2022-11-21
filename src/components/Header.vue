<template>
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Projetos</a></li>
        <li><a href="#">Contato</a></li>
    </ul>    
</template>
<script>
export default {
  name: "Header",
};
</script>

<style scoped>
    ul {
        list-style: none;
        display: flex;
        background-color: #000;
    }

    li {
        margin-right: 10px;
    }

    a {
        color: #DDD;
        text-decoration: none;
        transition: .3s;
    }

    a:hover {
        color: #888;
    }
</style>