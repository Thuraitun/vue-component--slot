<template>
    <h3 v-for="nama in nameLists" :key="nama.firstName">
        <slot :firstName="nama.firstName" :lastName="nama.lastName"></slot>
    </h3>
</template>

<script>
    export default {
        name: 'NameList',
        data() {
            return {
                nameLists: [
                    {
                        firstName: 'Thurai',
                        lastName: 'Tun',
                    },
                    {
                        firstName: 'David',
                        lastName: 'Lai',
                    },
                    {
                        firstName: 'SaiKham',
                        lastName: 'Rai',
                    },
                ]
            }
        }
    }
</script>

<style scoped>

</style>