<script>
  import HeroTotale from './components/HeroTotale.vue';
  import Navbar from './components/Navbar.vue';
  import CardComponents from './components/CardComponents.vue';
  import Contacts from './components/Contacts.vue';

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
      Contacts,
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
          <SaveButton />
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

    <section class="section-footer">
       <div class="footer row p-3">
          <div class="logo col">
            <a class="logo-big d-flex flex-column align-items-center px-3" href="#hero"> 
                <img class="img-logo" src="/images/logo-saketravel-white.svg" width="100" height="100">
                <h2>SAKE TRAVEL</h2>
                <h4 class="px-2">Your travel guide in Asia</h4>
            </a>
        </div>  

        <div class="contacts col">
          <Contacts
          Title="TELL US YOUR EXPERIENCE"
          Link1="https://www.google.com/"
          Name1="Link1"
          Link2="https://www.google.com/"
          Name2="Link2"
          Link3="https://www.google.com/"
          Name3="Link3"
          Link4="Link4"
          Name4="https://www.google.com/"
          />
        </div>

        <div class="contacts col">
          <Contacts
          Title="OUR FAVOURITES"
          Link1="https://www.google.com/"
          Name1="Link1"
          Link2="https://www.google.com/"
          Name2="Link2"
          Link3="https://www.google.com/"
          Name3="Link3"
          Link4="Link4"
          Name4="https://www.google.com/"
          />
        </div>
      </div>
    </section>
   
  </main>
</template>

<style scoped>

  .hero-background {
    width: 100vw;
    height: 100vh;
    background-image: url(/images/img-hero2.jpg);
    background-repeat: no-repeat;
    background-size: cover;
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

  .section-footer {
    width: 100vw;
    background-color: #1f2326;
  }

.section-footer p {
    color: white;
    font-weight: 200;
    font-size: 1.2rem;
    text-align: center;
}


.section-footer h2 {
    font-weight: 400;
    font-size: 2rem;
    text-align: center;
    color: white;
}

.section-footer h4 {
    font-weight: 200;
    font-size: 1.2rem;
    text-align: center;
    color: white;
}

.section-footer a:hover {
    background-color: #1f2326;
}
</style>
