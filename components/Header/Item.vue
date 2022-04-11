<script setup>
const items = [
  {
    text: "Кухонные ножи TUOTOWN",
  },
  {
    text: "Складные ножи TUOTOWN",
  },
  {
    text: "Кухонные ножи QXF",
  },
  {
    text: "Точильные камни",
  },
  {
    text: "Наборы для BBQ",
  },
  {
    text: "Кухонные принадлежности",
  },
  {
    text: "Туристические товары",
  },
];
</script>

<template>
  <div class="menu-item">
    <div v-for="item in items" :key="item">
      <router-link to="/product" class="menu-router">
        {{ item.text }}
      </router-link>
    </div>
  </div>
</template>

<style>
.menu-item {
  max-width: 370px;
  position: absolute;
  top: 0;
  left: 0;
  padding: 50px 30px;
}
.menu-item div {
  color: white;
  margin: 30px 10px;
}
.menu-router {
  list-style: none;
  text-decoration: none;
  color: white;
}
</style>
