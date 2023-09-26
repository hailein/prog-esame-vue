<script setup>
defineProps ({
    Title: String,
    Name1: String,
    Link1: String,
    Name2: String,
    Link2: String,
    Name3: String,
    Link3: String,
    Name4: String,
})


</script>

<template>

    <div class="contacts px-3">
        <h3> {{ Title }}</h3>
        <ul>
            <li> <a :href="Link1"> {{ Name1 }} </a> </li>
            <li> <a :href="Link2"> {{ Name2 }} </a> </li>
            <li> <a :href="Link3"> {{ Name3 }} </a> </li>
            <li> <a :href="Link4"> {{ Name4 }} </a> </li>
        </ul>
    </div>
    
</template>

<style scoped>

h3 {
    font-weight: 400;
    font-size: 1.5rem;
    color: white;
}


li {
    color: white;
    font-weight: 200;
    font-size: 1.2rem;
    list-style: none;
}
</style>
