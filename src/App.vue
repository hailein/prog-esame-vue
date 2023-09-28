<script>
  import HeroTotale from './components/HeroTotale.vue';
  import Navbar from './components/Navbar.vue';
  import CardComponents from './components/CardComponents.vue';
  import LinkAbout from './components/LinkAbout.vue';
  import LinkFavourite from './components/LinkFavourite.vue';
  import LinkContacts from './components/LinkContacts.vue';

  import contentsData from './assets/Contents.json';

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
      LinkAbout,
      LinkFavourite,
      LinkContacts,
    },
  };
</script>

<template>
  <header>

  </header>

  <main>
    <section class="section-hero" id="hero">
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

    <section class="section-cards" id="discover">

        <h2 class="title-cards"> Six japanese city you can't miss </h2>

      <div class="row" id="cards">
        <div class="col-lg-4 col-md-6 col-sm-12 mb-4" v-for="card in contents.cards" :key="card.id">
         <CardComponents
          :title="card.title"
          :description="card.description"
          :imageUrl="card.image_thumbnail"
          :url="card.url"
        />
        </div>
      </div>
    </section>

    <section class="section-footer" id="contacts">
      <div class="footer row">
          <div class="logo col-lg-3 col-md-12 col-sm-12 pb-5">
            <a class="logo-big d-flex flex-column align-items-center" href="#hero"> 
                <img class="img-logo" src="/images/logo-saketravel-white.svg" width="100" height="100">
                <h2 class="p-2">SAKE TRAVEL</h2>
                <h4>Your travel guide in Asia</h4>
            </a>
        </div>  

        <div class="favourites col-lg-3 col-md-4 col-sm-12 d-flex flex-column align-items-center pb-5">
          <div class="container-footer">
            <h4 class="text-start"> YOUR FAVOURITES </h4>
            <div class="favourite-links" v-for="favourite in contents.favourites" :key="favourite.id">
              <LinkFavourite
                  :name="favourite.name"
                  :url="favourite.url"
                  />
            </div>
          </div>
       </div>

        <div class="about-us col-lg-3 col-md-4 col-sm-12 d-flex flex-column align-items-center pb-5">
          <div class="container-footer">
            <h4 class="text-start"> ABOUT US </h4>
            <div class="about-us-links" v-for="about in contents.abouts" :key="about.id">
              <LinkAbout
                  :name="about.name"
                  :url="about.url"
                />
            </div>
          </div>  
        </div>

        <div class="contacts col-lg-3 col-md-4 col-sm-12 d-flex flex-column align-items-center pb-5">
          <div class="container-footer">
            <h4 class="text-start"> CONTACT US </h4>
            <div class="contact-links" v-for="contact in contents.contacts" :key="contact.id">
              <LinkContacts
                  :name="contact.name"
                  :url="contact.url"
                  :icon="contact.icon"
                />
            </div>
          </div>  
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

.footer {
  padding-top: 10%;
  padding-bottom: 5%;
  width: 100vw;
}


.section-footer h2 {
    font-weight: 400;
    font-size: 2rem;
    text-align: center;
    color: white;
}

.section-footer h4 {
    font-weight: 400;
    font-size: 1.2rem;
    text-align: center;
    color: white;
}

.section-footer a:hover {
    background-color: #1f2326;
}

</style>
