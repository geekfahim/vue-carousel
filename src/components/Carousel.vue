<script setup>
import { onMounted, ref } from "vue";

const images = ref([
"https://images.unsplash.com/photo-1451187580459-43490279c0fa?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1172&q=80",
"https://images.unsplash.com/photo-1531297484001-80022131f5a1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1120&q=80",
"https://images.unsplash.com/photo-1515704089429-fd06e6668458?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
"https://images.unsplash.com/photo-1543147495-b6984a841135?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1138&q=80",
"https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80"

])
// const sliderImage = ref([
//     "https://images.unsplash.com/photo-1684254149400-22d7eaec54ca?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=871&q=80"
// ])

// function setSliderImage(img) {
//     sliderImage.value = img
// }
// const flkty = new Flickity( '.main-carousel')

onMounted(()=>{
    const carousel = new Flickity( '.main-carousel')
});

</script>

<template>
    <div class="main-carousel">
        <div  class="item" :style="`background-image:url(${image})`" v-for="(image, index) in images" :key="index">{{ index }}</div>
    </div>
</template>

<style scoped>
.main-carousel {
    width: 100%;
}
.item {
    width: 100%; 
    height: 500px;
    background-size: cover;
    background-position: center;

}

</style>