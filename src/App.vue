<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>

    <div class="wrapper">
      <nav>
        <h3><RouterLink to="/" :style="{textDecoration: 'none', color: 'black'}">Home</RouterLink></h3>
        <h3><RouterLink to="/books" :style="{textDecoration: 'none', color: 'black'}">Books </RouterLink></h3>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>




nav h3 {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav h3:hover{
  text-decoration: underline;
}

.wrapper {
  background-color: grey;
  width: 100%;
}

@media screen and (max-width: 600px) {
  .wrapper{
    width:auto;
    background-color: grey;

  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
    
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
