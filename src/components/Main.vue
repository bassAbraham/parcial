<script setup lang="ts">
import type { Emisoras } from '@/App.vue';

defineProps<{
  emisoras: Emisoras[]
}>()
</script>

<template>
    <main>
        <section class="emisora-imagen">
            <div class="container-imgs">
                <div v-for="emisora in emisoras" :key="emisora.id">
                    <img class="img-emisora" :src="emisora.imagen" :alt="emisora.nombre">
                </div>
            </div>
        </section>
        <section class="emisora-lista">
            <div class="container-name-emisora" v-for="emisora in emisoras" :key="emisora.id">
                <p>{{ emisora.nombre }}</p>
            </div>
        </section>
    </main>
</template>

<style scoped>
main {
    background-color: #1C313A;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
}

.emisora-imagen {
    grid-column-start: 1;
    grid-column-end: 3;
}

.emisora-lista {
    background-color: #21404B;
    display: grid;
    gap: 5px;
    padding: 7px;
}

.container-name-emisora {
    padding: 5px 0 5px 0;
    background-color: #455A64;
    display: flex;
    justify-content: center;
}

.container-name-emisora:hover {
    background-color:  #697A82;
}

p {
    color: white;
    font-family: "Roboto", sans-serif;
    font-weight: 300;
    font-style: normal;
}

.img-emisora {
    height: 170px;
    width: 100%;
}
.container-imgs {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
}
</style>