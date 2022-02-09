<template>
  <main>
      <div class="container">
          <div class="posts-container">
              <div class="posts-grid">
                  <div>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ea tempora nobis esse doloribus cumque magni temporibus aliquid. Quaerat reprehenderit quia nostrum quam! Ea ipsum quia architecto voluptates dignissimos dolorum incidunt.</div>
                  <div>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ea tempora nobis esse doloribus cumque magni temporibus aliquid. Quaerat reprehenderit quia nostrum quam! Ea ipsum quia architecto voluptates dignissimos dolorum incidunt.</div>
                  <div>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ea tempora nobis esse doloribus cumque magni temporibus aliquid. Quaerat reprehenderit quia nostrum quam! Ea ipsum quia architecto voluptates dignissimos dolorum incidunt.</div>

              </div>
          </div>
      </div>
  </main>
</template>

<script>
export default {
    name: 'Posts'
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
        }
    }
}
</style>
