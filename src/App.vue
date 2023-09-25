<script>
  import HeroTotale from './components/HeroTotale.vue';
  import Navbar from './components/Navbar.vue';
  import CardComponents from './components/CardComponents.vue';

  import contentsData from './assets/contents.json';

export default {
  data() {
      return {
        contents: contentsData,
      };
    }, 

    components: {
      CardComponents,
      HeroTotale,
      Navbar,
    }, 
  };
</script>

<template>
  <header>

  </header>

  <main>
    <section class="section-hero">
      <Navbar/>
        <div class="hero-background d-flex align-items-end justify-content-center">
          <HeroTotale
          title="DISCOVER JAPAN"
          subtitle="The best destinations in the most ancient country" 
          cta="Scroll to see more"
          icon="icon"
          />
        </div>
    </section>

    <section class="section-cards">

        <h2 class="title-cards"> Six japanese city you can't miss </h2>
        <!-- <SaveButton /> -->
      <div class="row justify-content-center" id="cards">
        <div class="col-lg-4 col-md-6 colsm-12" v-for="card in contents.cards" :key="card.id">
         <CardComponents
          :title="card.title"
          :description="card.description"
          :imageUrl="card.image_thumbnail"
          :url="card.url"
        />
      </div>
      </div>
    </section>
   
  </main>
</template>

<style scoped>

  svg {
    fill: pink;
    width: 10vh;
  }

  .hero-background {
    width: 100vw;
    height: 100vh;
    background-image: url(/images/img-hero2.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    margin-top: -10vh;
    padding-bottom: 10vh;
  }

  .title-cards {
    font-weight: 600;
    font-size: 4rem;
    color: #1f2326;
    text-align: center;
    padding: 3%;
  }
  .section-cards {
    padding: 5%;
    width: 100vw;
  }

</style>
