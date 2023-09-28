<script setup>

</script>

<template>
<nav class="navbar fixed-top navbar-expand-lg d-flex align-items-center">
  <a class="navbar-brand d-flex align-items-center pb-4 pt-4" href="#hero"> 
    <img class="logo" src="/images/logo-sake-travel.svg" width="30" height="30">
    <p class="px-2">SAKE TRAVEL</p>
  </a>
  
  <div class="collapse navbar-collapse">
    <ul class="navbar-nav">
      <li class="nav-item">
        <a class="nav-link" href="#discover">Discover</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#contacts">Contact us</a>
      </li>
    </ul>
  </div>
</nav>
</template>

<style scoped>

.navbar {
  background-color: rgba(255, 255, 255, 0.75);
  height: 10vh;
  font-weight: 200;
  font-size: 1.2rem;
  color: #1f2326;
}

a {
  color: #1f2326;
  height: 100%;
  margin-left: 10px;
}

a:hover {
  background-color: #c7ccd9;
  color: #1f2326;
}

p {
  display: inline-block;
  vertical-align: middle;
  margin: 0;
}

</style>
