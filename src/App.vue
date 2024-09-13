<script setup lang="ts">
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';

import {onMounted, ref} from 'vue'
import axios from 'axios';

export interface Emisoras {
    id: string
    nombre: string
    imagen: string
}

const emisoras = ref<Emisoras[]>([])

onMounted(() => {
    (async () => {
        const response = await axios.get("https://cobuses.com.co/APIV2/model/radio.php?dato=getallemisoras")
        emisoras.value = response.data
        console.log(response.data)
    })()
})

</script>

<template>
<div>
    <Header></Header>
    <Main :emisoras="emisoras"></Main>
    <Footer></Footer>
</div>
</template>

<style scoped>

</style>
