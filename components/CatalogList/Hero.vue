<template>
  <div class="catalog__hero">
    <img :src="catalogHeroImage" alt="Catalog Image" />
    <h1>Дом и Ножи</h1>
    <p>Эксклюзивные технологии на страже чистоты и уюта в вашем доме</p>
  </div>
</template>

<script setup>
import catalogHeroImage from "@/assets/catalog-hero.jpg";
</script>

<style scoped>
.catalog__hero {
  position: relative;
}
.catalog__hero h2 {
  position: absolute;
  text-align: center;
  width: 100%;
  top: 45%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.catalog__hero p {
  position: absolute;
  text-align: center;
  width: 100%;
  top: 55%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-family: "Montserrat";
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 20px;
  color: #ffffff;
}
.catalog__hero img {
  max-width: 100%;
  width: 100%;
}
</style>
