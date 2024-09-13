<template>
    <header>
        <nav class="nav-header">
            <li>EMISORAS</li>
            <li>PODCASTS</li>
            <li>MI LISTA</li>
            <li>BUSQUEDA</li>
        </nav>
    </header>
</template>

<script setup lang="ts">

</script>

<style scoped>

header {
    box-sizing: border-box;
}

.nav-header {
    display: flex;
    align-items: center;
    background-color:  #455A64;
}

li {
    flex: 1;
    padding: 25px 0 25px 0;
    color: white;
    list-style: none;
    display: flex;
    justify-content: center;
    font-family: "Roboto", sans-serif;
    font-weight: 300;
    font-style: normal;
}

li:hover {
    border-bottom: 1px solid white;
   
}
</style>