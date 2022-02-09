<template>
    <div class="post-card">
        <div class="post-img">
            img Placeholder
        </div>
        <div class="post-content">
          <a href="#"><h3>{{ post.title }}</h3></a>
          <p class="main-content-post">
            {{ extractText }}
          </p>
        </div>
        <div class="post-details">
            {{ getDate }}
        </div>
    </div>
</template>

<script>

import dayjs from "dayjs";

export default {
    name: 'PostItem',
    props:{
        'post': Object
    },
    computed: {
        extractText(){
            return this.post.content.substr(0, 60) + '...';
        },
        getDate(){
            const date = new Date(this.post.created_at);
            return dayjs(date).format("YYYY-MM-DD");
        }
    },
}
</script>

<style lang="scss" scoped>
.post-card {
    background-color: red;
}
</style>
