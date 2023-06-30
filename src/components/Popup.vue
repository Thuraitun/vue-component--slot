<template>
    <div>
        <h2>Popup Component</h2>
        <button @click="$emit('close', 'Thurai')">Popup Close</button>
    </div>
</template>

<script>
    export default {
        name: 'Popup',
        emits: ['close'],
    }
</script>

<style scoped>

</style>