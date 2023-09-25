<script setup>
defineProps({
    title: String,
    description: String,
    imageUrl: String,
    url: String,
})
</script>

<template>
    <div class="card">
        <h3>{{ title }}</h3> 
       <div class="image-container">
            <a :href="url" target="_blank" rel="noopener noreferrer"> <img :src="imageUrl" alt="" class="image"> </a>
       </div>
        <p class="description">
        {{ description }}
        </p>
    </div>

</template>

<style scoped>

h3 {
    text-transform: uppercase;
    font-weight: 600;
    font-size: 2rem;
    color: #1f2326;
    text-align: center;
}

p {
  font-weight: 200;
  font-size: 1.2rem;
  color: #1f2326;
  padding-top: 15px;
}

.image {
    width: 100%;
    padding-top: 10px;
}

.card:hover {
    scale: 108%;
}

.card {
    margin: 5%;
    padding: 5%;
    border: solid 1px #1f23262d;
    border-radius: 8%;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    transition: 0.3s;
}
</style>
