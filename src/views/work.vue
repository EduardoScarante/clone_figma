<script>

import worksComp from '../components/worksComp.vue';

export default {
  components: {
    worksComp
  },
  data() {
    return {
      infos: [
        {
          imagePath: "imagePath",
          Title: "Title",
          subTitle: "subTitle"
        }
      ]
    }
  }
}
</script>

<template>
<main>
  work view

  <worksComp
    :imagePath='infos[0].imagePath'
    :Title='infos[0].Title'
    :subTitle='infos[0].subTitle'
  />

</main>
</template>

<style scoped>
main{
  height: 200px;
  background-color: lightgreen;
}

</style>
