<template>
    <div class="app">
        <post-form            
            @create="createPost"/>
        <post-list 
            :posts="posts"
        />
    </div>
</template>

<script>
    import PostForm from "@/components/PostForm";
    import PostList from "@/components/PostList";

    export default{
        components: {
                PostList,
                PostForm
        },
        data(){
            return{
                posts:[
                    {id:1, title: 'Title', body: 'desc'},
                    {id:2, title: 'Title 2', body: 'desc 2'},
                    {id:3, title: 'Title 2', body: 'desc 3'},
                ],
            title: '',
            body: ''
            }
        },
        methods: {
            createPost(post){
                this.posts.push(post);
            },
        }
    }
</script>

<style> 
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.app {
    padding: 20px;
}
</style>
