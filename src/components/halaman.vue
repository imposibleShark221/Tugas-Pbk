<script setup>
    import { ref } from 'vue'

    const nama = ref('Ari')
    nama.value = 'Kristian'

    const name = ref('Mahasiswa')

    const nilai = ref(0)

    function increment(){
        nilai.value++
    }

   const text = ref('')

   const kondisi = ref(0)

   function ubah(){
    kondisi.value = !kondisi.value
   }

</script>

<template>
    <h1>{{ nama }}</h1>
    <h1>{{ nama }} adalah seorang {{ name }}</h1>

    <button v-on:click="increment">hitung : {{ nilai }}</button>

    <input v-model="text">
   <p>{{ text }}</p>

   <button v-on:click="ubah">ubah disini</button>
   <h1 v-if="kondisi">Vue is Good</h1>
   <h1 v-else>Vue is mid</h1>

</template>