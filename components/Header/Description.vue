<script setup>
const items = [
  {
    text: "Новости",
  },
  {
    text: "О компании",
  },
  {
    text: "Контакты",
  },
  {
    text: "Как проехать",
  },
];
</script>

<template>
  <div class="menu-description">
    <div v-for="item in items" :key="item">
      <router-link to="/" class="menu-description-router">
        {{ item.text }}</router-link
      >
    </div>
  </div>
</template>

<style>
.menu-description {
  position: absolute;
  color: white;
  opacity: 0.5;
  bottom: 0;
  left: 0;
  padding: 0 0 150px 30px;
}
.menu-description div {
  margin: 10px 10px;
}
.menu-description-router {
  list-style: none;
  text-decoration: none;
  color: white;
  opacity: 0.5;
}
@media screen and (max-width:376px) {
  .menu-description {
    bottom: -60px;
  }
}
</style>
