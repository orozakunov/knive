<script setup>
const catalog = ["Кухонные ножи", "Складные ножи", "Точилки для ножей"];
</script>

<template>
  <div class="catalog">
    <h3>Каталог</h3>
    <div class="catalogList">
      <li class="catalogList-li" v-for="item in catalog" :key="item">
        {{ item }}
      </li>
    </div>
  </div>
</template>

<style>
h3 {
  margin: 20px 0;
  font-weight: 500;
  font-size: 18px;
  color: #ffffff;
}
.catalogList {
  width: 427px;
  color: white;
  list-style: none;
  display: flex;
  opacity: 0.5;
  align-items: center;
}
.catalogList-li {
  padding-top: 15px;
  margin: 0 5px;
}

@media screen and (max-width: 376px) {
  .catalogList-li {
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    margin: 0 5px;
  }
  .catalogList-li:first-child {
    margin: 0;
  }
}
</style>
