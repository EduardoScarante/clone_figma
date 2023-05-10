<script>
import { RouterLink, RouterView } from 'vue-router'

import HomeView from './views/HomeView.vue'

export default{
  methods:{
    scroll(){
      window.scrollTo(0, 1000)
      console.log("yes");
    }
  }
}

</script>

<template>
  <header>
    <a href="">logo</a>
    <nav>
      <a href="">About</a>
      <a href="">Work</a>
      <a href="">Contact</a>
    </nav>
  </header>

  <HomeView/>

  <RouterView />

</template>

<style scoped>
header{
  display: flex;
  justify-content: space-between;
  align-items: center;
}

header a{
  padding: 20px;
  text-decoration: none;
  color: black;
}

header a:hover{
  opacity: 0.8;
}

</style>
