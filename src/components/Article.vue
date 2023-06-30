<template>
    <div>
        <h2>Aritcle Component</h2>
        <h2 v-bind="$attrs">{{ title }}</h2>
        <h2>Likes is {{ likes }}</h2>
        <h2>Published is {{ isPublished ? 'Yes' : 'No'}}</h2>
    </div>
</template>

<script>
    export default {
        name: 'Article',
        props: { 
            title: {
                type: String,
                required: true,
                default: 'Article Default Title',
            },
            likes: Number,
            isPublished: Boolean,
        },
        inheritAttrs: false,
        data() {
            return {

            }
        },
    }
</script>

<style scoped>

</style>