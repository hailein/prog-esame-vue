<script>
  import HeroTotale from './components/HeroTotale.vue';
  import Navbar from './components/Navbar.vue';

  // import contentsData from './assets/contents.json'

export default {
    /* data() {
      return {
        contents: contentsData,
      };
    }, */

    components: {
      HeroTotale,
      Navbar,
    }, 
  };
</script>

<template>
  <header>
  
  </header>

  <main>
    <div class="home">
      <Navbar/>
      <div class="hero-background d-flex align-items-end justify-content-center">
        <HeroTotale
        title="DISCOVER JAPAN"
        subtitle="The best destinations in the most ancient country" 
        cta="Scroll to see more"
        icon="icon"
        />

      </div>
    </div>
   
  </main>
</template>

<style scoped>
  .hero-background {
    width: 100vw;
    height: 100vh;
    background-image: url(./assets/images/img-hero2.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    margin-top: -10vh;
    padding-bottom: 10vh;
  }
</style>
