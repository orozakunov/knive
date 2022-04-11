<script setup>
import Catalog from "./Catalog.vue";
import Social from "./Social.vue";

const information = ["Главная", "Новости", "О компании"];
</script>

<template>
  <div class="information">
    <div class="info">
      <h3 class="information-h3">Информация</h3>
      <div class="informationList">
        <li class="information-li" v-for="item in information" :key="item">
          {{ item }}
        </li>
      </div>
    </div>
    <Catalog />
    <Social />
  </div>
</template>

<style>
.information {
  padding: 0 102px 0 64px;
  width: 385px;
}
.information-h3 {
  font-weight: 600;
  font-size: 17px;
  color: white;
}
.information-li {
  font-size: 14px;
  margin: 20px 20px;
}
.information-li:first-child {
  margin: 0;
}
.informationList {
  align-items: center;
  color: white;
  list-style: none;
  display: flex;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .information {
    padding: 0;
  }
}
</style>
