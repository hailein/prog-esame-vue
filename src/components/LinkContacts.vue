<script setup>
defineProps ({
    name: String,
    url: String,
    icon: String,
})
</script>

<template>

    <div class="link pb-2">
        <a :href="url" target="_blank" rel="noopener noreferrer" class="d-flex"> 
            <!-- <img :src="icon" width="30" height="30" alt="icon-social"> -->
            <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="30" height="30" viewBox="0,0,256,256">
            <g fill="#ffffff" fill-rule="nonzero" stroke="none" stroke-width="1" stroke-linecap="butt" stroke-linejoin="miter" stroke-miterlimit="10" stroke-dasharray="" stroke-dashoffset="0" font-family="none" font-weight="none" font-size="none" text-anchor="none" style="mix-blend-mode: normal"><g transform="scale(5.12,5.12)"><path :d="icon"></path></g></g>
            </svg>
             <p> {{ name }}</p> 
        </a>
    </div>
    
</template>

<style scoped>

p {
    color: white;
    font-weight: 200;
    font-size: 1.2rem;
    transition: 0.2s;
    padding-left: 6%;
    display: flex;
    align-items: center;
    margin: 0;
}

svg {
    fill: white;
}

a:hover {
    scale: 108%;
}
</style>
