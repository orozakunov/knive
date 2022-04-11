<template>
  <div class="container">
    <div class="collection__secondary">
      <div v-for="item in images" :key="item" class="item">
        <Item :image="item"/>
      </div>
    </div>
  </div>
</template>

<script setup>
import Item from "../CollectionItems/SecondaryItem.vue";

const images = [
  {
    imageUrl: "../src/assets/secondary-collection-item-1.png",
  },
  {
    imageUrl: "../src/assets/secondary-collection-item-2.png",
  },
  {
    imageUrl: "../src/assets/secondary-collection-item-3.png",
  },
  {
    imageUrl: "../src/assets/secondary-collection-item-4.png",
  },
  {
    imageUrl: "../src/assets/secondary-collection-item-5.png",
  },
  {
    imageUrl: "../src/assets/secondary-collection-item-6.png",
  },
  {
    imageUrl: "../src/assets/secondary-collection-item-7.png",
  },
  {
    imageUrl: "../src/assets/secondary-collection-item-8.png",
  },
];
</script>

<style scoped>
@media (max-width: 320px) {
  .collection__secondary .item {
    display: none;
  }
}

.container {
  margin: 0 auto;
  max-width: 1300px;
}
.collection__secondary {
  display: flex;
}
.item {
  margin: 0 20px;
}
</style>