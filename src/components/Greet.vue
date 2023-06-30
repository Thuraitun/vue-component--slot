<template>
    <h2>Hello I am {{ name }}. Hero Name is {{ heroName }}</h2>
</template>

<script>
    export default {
        name: "Greet",
        props: ['name', 'heroName'],
    }
</script>

<style scoped>

</style>