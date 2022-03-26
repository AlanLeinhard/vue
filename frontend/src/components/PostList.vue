<template>
    <div>
        <h3>Users</h3>
        <post-item class="post" v-for="post in posts"/>
            <div><strong>Title</strong> {{ post.title }}</div>
            <div><strong>Body</strong> {{ post.body }}</div>
    </div>
</template>

<script>
    export default {
        props: {
            posts:{
                type: Array,
                required: true
            }
        }
    }
</script>

<style>

.post {
    padding: 15px;
    border: 2px solid teal;
    margin: 15px;
}
</style>