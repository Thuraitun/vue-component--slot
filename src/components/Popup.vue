<template>
    <div>
        <h2>Popup Component</h2>
        <input type="text" v-model="name">
        <button @click="$emit('close', name)">Popup Close</button>
    </div>
</template>

<script>
    export default {
        name: 'Popup',
        emits: {
            close: (name) => {
                if(!name) {
                    return false
                } else {
                    return true 
                }
            }
        },
        data() {
            return {
                name: '',
            }
        },
    }
</script>

<style scoped>

</style>