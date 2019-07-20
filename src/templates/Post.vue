<template>
    <BlogLayout>
        <div v-html="$page.post.content"></div>
    </BlogLayout>    
</template>


<page-query>
 query Post($path: String!){
     post: post(path: $path){
         title
         content
     }
 }   
</page-query>


<script>
export default {
    metaInfo(){
        return {
            title: this.$page.post.title
        }
    }
}
</script>

