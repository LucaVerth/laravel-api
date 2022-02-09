<template>
  <header>
      <div class="container">
          <nav class="navbar">
              <ul>
                  <li><a href="#">Home</a></li>
                  <li><a class="active" href="#">Blog</a></li>
                  <li><a href="#">About us</a></li>
                  <li><a href="#">Contacts</a></li>
              </ul>
          </nav>
      </div>
  </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style lang="scss" scoped>
header{
    display: flex;
    align-items: center;
    height: 110px;
    background-color: red;
    .navbar{
        background-color: rgba(0, 0, 0, 0.6);
        ul{
            display: flex;
            justify-content: space-evenly;
            list-style: none;
            a{
                text-decoration: none;
                color: #fff;
                &:hover{
                    text-decoration: underline;
                    color: red;
                    transition: all 0.2s ease-out;
                }
                &.active{
                    color: blue;
                }
            }
        }
    }
}
</style>
