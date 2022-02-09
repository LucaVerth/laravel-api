<template>
  <main>
      <div class="container">
          <div class="posts-container">
              <div class="posts-grid">
                  <PostItem
                    v-for="post in posts"
                    :key="post.id"
                    :post="post"
                  />
              </div>
          </div>
      </div>
  </main>
</template>

<script>

import PostItem from './PostItem.vue';

export default {
    name: 'Posts',
    components:{
        PostItem,
    },
    data(){
        return {
            apiUrl: 'http://127.0.0.1:8000/api/posts',
            posts: null,

        }
    },
    mounted(){
        this.getPosts();
    },
    methods:{
        getPosts(){
            axios.get(this.apiUrl)
            .then(res=>{
                this.posts = res.data;
                console.log(this.posts);
            })
            .catch(function (error) {
                console.log(error);
            })
        }
    },

}
</script>

<style lang="scss" scoped>
main{
    min-height: calc(100vh - 210px);
    background-color: gold;
    .posts-container{
        padding: 3rem 0;
        .posts-grid{
            display: grid;
            gap: 1.3rem;
            grid-template-columns: repeat(3, 1fr);
            grid-template-rows: auto;
        }
    }
}
</style>
