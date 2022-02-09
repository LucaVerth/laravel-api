<template>
    <div class="post-card">
        <div class="post-img">
            img Placeholder
        </div>
        <div class="post-content">
          <a href="#"><h3>{{ post.title}}</h3></a>
          <p class="main-content-post">
            {{post.content}}
          </p>
        </div>
        <div class="post-details">
            {{post.created_at}}
        </div>
    </div>
</template>

<script>
export default {
    name: 'PostItem',
    props:{
        'post': Object
    },
}
</script>

<style lang="scss" scoped>
.post-card {
    background-color: red;
}
</style>
