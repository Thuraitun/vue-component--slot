<template>
    <h3>Tab C Component</h3>
    <input type="text" v-model="userName" />
</template>

<script>
    export default {
        name:'TabC',
        data() {
            return {
                userName: '',
            }
        }
    }
</script>

<style scoped>

</style>