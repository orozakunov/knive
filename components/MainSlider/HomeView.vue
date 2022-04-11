<script setup>
import Carousel from "./Carousel.vue";
import Slide from "./Slide.vue";
const carouselSlides = ["slide1", "slide2", "slide3"];
</script>

<template>
  <div class="home">
    <Carousel class="carousel" v-slot="{ currentSlide }">
      <Slide v-for="(slide, index) in carouselSlides" :key="index">
        <div v-show="currentSlide === index + 1" class="slide-info">
          <img :src="`/assets/${slide}.png`" alt="" />\
          <!-- src/assets/Basket/${slide}.png -->
        </div>
      </Slide>
    </Carousel>
  </div>
</template>

<style scoped>
.carousel {
  max-height: 100vh;
  height: 590px;
}
.slide-info {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 590px;
}
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
@media (max-width: 768px) {
  img {
    width: 768px;
    height: 480px;
  }
}
@media (max-width: 390px) {
  img {
    width: 390px;
    height: 480px;
  }
}
@media screen and (max-width: 376px) {
  img {
    width: 375px;
    height: 400px;
  }
  .carousel {
    height: 390px;
  }
}
</style>
