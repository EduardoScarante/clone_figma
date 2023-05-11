<script>
import { RouterLink, RouterView } from 'vue-router'

import HomeView from './views/HomeView.vue'
</script>

<template>
  <header>
    <a id="logo" href="">Visual Design :)</a>
    <nav>
      <a href="">About</a>
      <a href="">Work</a>
      <a href="">Contact</a>
    </nav>
  </header>

  <HomeView />

  <RouterView />
</template>

<style scoped>
#logo {
  font-weight: 800;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
}

header {
  position: sticky;
  top: 0px;
  z-index: 1;

  background-color: rgb(255, 255, 255, 0.85);

  display: flex;
  justify-content: space-between;
  align-items: center;
}

header a {
  padding: 20px;
  text-decoration: none;
  color: black;
}

header a:hover {
  opacity: 0.8;
}

@media (max-width: 600px) {
  header>nav {
    display: none;
  }

  header {
    align-items: center;
    justify-content: center;
  }
}
</style>
