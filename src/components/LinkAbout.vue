<script setup>
defineProps ({
    name: String,
    url: String,
})
</script>

<template>

    <div class="link pb-1.5">
        <a :href="url" target="_blank" rel="noopener noreferrer"> {{ name }} </a>
    </div>
    
</template>

<style scoped>

a {
    color: white;
    font-weight: 200;
    font-size: 1.2rem;
    transition: 0.2s;
}

a:hover {
    text-decoration: underline solid white;
}
</style>
