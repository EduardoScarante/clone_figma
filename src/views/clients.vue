<script>

import clientsComp from '../components/clientsComp.vue';

import img1 from '@/assets/clients/img1.png'
import img2 from '@/assets/clients/img2.png'
import img3 from '@/assets/clients/img3.png'


export default {
  components: {
    clientsComp
  },
  data() {
    return {
      infos: [
        {
          imagePath: img1,
          title: "This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com",
          name: "Gemma Nolen, Google"
        },
        {
          imagePath: img2,
          title: "This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com",
          name: "Gemma Nolen, Google"
        },
        {
          imagePath: img3,
          title: "This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com",
          name: "Gemma Nolen, Google"
        }
      ]
    }
  }
}

</script>

<template>
  <p>Clients</p>
  <main id="container">
    <div v-for="x in infos" id="content">
      <clientsComp :imagePath="x.imagePath" :title="x.title" :name="x.name" />
    </div>
  </main>
</template>

<style scoped>
#container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

p {
  margin-top: 100px;
  width: 100%;
  text-align: center;

  font-weight: 600;
  font-size: 2rem;
}
</style>
