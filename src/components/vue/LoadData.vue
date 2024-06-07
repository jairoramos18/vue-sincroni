<script setup>

function loadData() {
    fetch('https://jsonplaceholder.typicode.com/users')
        .then(function (response) {
            return response.json()
        })
        .then(function (data) {
            console.log(data)
        })
}

</script>

<template>
    <div class="bg-slate-300 mb-1">
        sjdl afaoldñ
    </div>
    <button @click="loadData">
        Cargar info
    </button>
</template>