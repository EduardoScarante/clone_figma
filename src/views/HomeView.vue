<script setup>

import brands from '@/views/brands.vue';
import skills from '@/views/skills.vue';
import work from '@/views/work.vue';
import clients from '@/views/clients.vue';
import forms from '@/views/forms.vue';

</script>

<template>
  <main>
    <section id="hero">
      <div class="content">
        <h2>Branding | Image Making</h2>
        <h1>Visual Designer</h1>
        <p>
          This is a template Figma file, turned into code using Anima. Learn
          more at AnimaApp.com
        </p>
      </div>
      <div class="img-container">
        <img src="@/assets/hero.png" alt="" />
      </div>
    </section>


    <section>
      <brands />
    </section>

    <section>
      <skills />
    </section>

    <section>
      <work />
    </section>

    <section>
      <clients />
    </section>

    <section>
      <forms />
    </section>
  </main>
</template>

<style scoped>
main {
  width: 100%;
  margin: 0;
  padding: 0;

  display: flex;
  flex-direction: column;
  justify-content: center;

}

#hero {
  display: flex;
  justify-content: center;
  height: 80vh;
}

.content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  font-family: "Epilogue", sans-serif;

  width: 50%;

  padding: 2rem 5rem;

}

.content h1 {
  font-weight: 600;
  font-size: 6rem;
  line-height: 6.5rem;
}

.content h2 {
  font-weight: 600;
  font-size: 1.5rem;
}

.content p {
  font-size: 1.2rem;
}

.img-container {
  display: flex;

  justify-content: center;
  align-items: center;

  height: 100%;
  width: 50%;
}

.img-container img {
  height: 80%;
}

@media (max-width: 600px) {
  #hero {
    flex-direction: column;
    height: 100%;
    width: 100vw;

    align-items: center;

    padding-bottom: 40px;

  }

  #hero img {
    width: 70%;
  }

  .img-container {
    width: 100%;
  }

  .content {
    padding: 2rem;
    width: 100%;

  }

  .content h1 {
    font-size: 4rem;
    line-height: 6.5rem;
  }
}
</style>