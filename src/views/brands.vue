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

  flex-wrap: wrap;

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
    height: 100%;
  }

  #content img {
    padding: 30px;

    width: 50% * max-content;
  }
}
</style>
