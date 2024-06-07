<script setup>
import { ref } from 'vue';

const users = ref([])
function loadData() {
    fetch('https://jsonplaceholder.typicode.com/users')
        .then(function (response) {
            return response.json()
        })
        .then(function (data) {
            console.log(data)
            users.value = data
        })
}

</script>

<template>
    <div v-for="(user,index) in users" :key="index.id"  class="bg-slate-300 mb-1">
       {{ user.name }}
    </div>
    <button @click="loadData">
        Cargar info
    </button>
</template>