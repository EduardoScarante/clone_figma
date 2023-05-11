<script>

import worksComp from '../components/worksComp.vue';

/* IMPORT IMAGES */
import img1 from '@/assets/works/img1.png'
import img2 from '@/assets/works/img2.png'
import img3 from '@/assets/works/img3.png'
import img4 from '@/assets/works/img4.png'
import img5 from '@/assets/works/img5.png'
import img6 from '@/assets/works/img6.png'

export default {
  components: {
    worksComp
  },
  data() {
    return {
      infos: [
        {
          imagePath: img1,
          Title: "Project title",
          subTitle: "UI, Art drection"
        },
        {
          imagePath: img2,
          Title: "Project title",
          subTitle: "UI, Art drection"
        },
        {
          imagePath: img3,
          Title: "Project title",
          subTitle: "UI, Art drection"
        },
        {
          imagePath: img4,
          Title: "Project title",
          subTitle: "UI, Art drection"
        },
        {
          imagePath: img5,
          Title: "Project title",
          subTitle: "UI, Art drection"
        },
        {
          imagePath: img6,
          Title: "Project title",
          subTitle: "UI, Art drection"
        },

      ]
    }
  },
  methods: {
    teste() {
      console.log("mesnagem bonita");
    }
  }
}
</script>

<template>
  <p>Latest Work</p>
  <div class="main">
    <div id="cards" v-for="x in infos">
      <worksComp :imagePath='x.imagePath' :Title='x.Title' :subTitle='x.subTitle' />
    </div>
  </div>
</template>

<style scoped>
.main {
  width: 100%;
  height: auto;

  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

#cards {
  width: 330px;
  height: 450px;
}

p {
  font-size: 2rem;
  font-weight: 600;
  text-align: center;
  padding: 30px;
}

@media (max-width: 600px) {
  .main {
    justify-content: center;
  }
}
</style>
