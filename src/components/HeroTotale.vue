<script setup>
defineProps({
  title: String,
  subtitle: String,
  cta: String,
  icon: String,
})
</script>

<template>
  <div id="hero">
    <div class="title-hero">
      <h1>{{ title }}</h1> 
      <h2> {{ subtitle }} </h2>
    </div>
      <div class="cta-scroll d-flex justify-content-center"> 
        <p class="cta"> {{ cta }} </p>
        <img src="/images/icon-scroll.png" alt="" class="icon-image"  width="50" height="50"> 
      </div>
  </div>
</template>

<style scoped>

h1 {
  font-weight: 600;
  font-size: 5rem;
  color: white;
  text-align: center;
  padding: 0;
  opacity: 80%;
}

h2 {
  text-align: center;
  padding: 0;
  font-weight: 200;
  font-size: 1.5rem;
  /* color: #1f2326; */
  color: white;
  opacity: 80%;
}



.cta {
  padding-top: 10px;
  padding-right: 5px;
  font-size: 1.5rem;
  font-weight: 200;
  color: white;
}

</style>
