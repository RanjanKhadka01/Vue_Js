<template>
    <h2>Article Component</h2>
    <h3>{{title}}</h3>
    <h3>Likes: {{likes}}</h3>
    <h3>Published: {{isPublished ? 'Yes' : 'No'}}</h3>
</template>

<script>
    export default {
        name: 'Article',
        props: {
            title: String,
            likes: Number,
            isPublished: Boolean,
        }
    }
</script>

<style scoped>

</style>