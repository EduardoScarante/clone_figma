<script>

import skillsComponent from '../components/skillsComponent.vue'

/* IMPORT IMAGES */
import img1 from '@/assets/skills/img1.png'
import img2 from '@/assets/skills/img2.png'
import img3 from '@/assets/skills/img3.png'

export default {
  components: {
    skillsComponent
  },
  data() {
    return {
      infos: [
        {
          imagePath: img1,
          title: "Product design",
          subtitle: "This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com"
        },
        {
          imagePath: img2,
          title: "Art direction",
          subtitle: "This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com"
        },
        {
          imagePath: img3,
          title: "Visual design",
          subtitle: "This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com"
        }
      ]
    }
  }
}

</script>

<template>
  <main id="main">
    <div id="card" v-for="x in infos">
      <skillsComponent :path="x.imagePath" :title="x.title" :subtitle="x.subtitle" />
    </div>
  </main>
</template>

<style scoped>
#main{

  
  display: flex;
  flex-direction: row;
}

#card {
  width: 100%;
}
</style>
