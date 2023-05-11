<script>

</script>

<template>
  <main id='content'>
    <img src="@/assets/brands/google.png" alt="">
    <img src="@/assets/brands/nike.png" alt="">
    <img src="@/assets/brands/sans.png" alt="">
    <img src="@/assets/brands/aplle.png" alt="">
    <img src="@/assets/brands/intercom.png" alt="">
    <img src="@/assets/brands/adidas.png" alt="">
  </main>
</template>

<style scoped>
#content {
  height: 180px;


  display: flex;
  flex-direction: row;

  justify-content: space-around;
  align-items: center;
}

main img {
  width: max-content;
}

@media (max-width: 600px) {
  #content {
    width: 100vw;
    flex-wrap: wrap;
  }
}
</style>
