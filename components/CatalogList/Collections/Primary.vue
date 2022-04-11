<template>
  <div class="container">
    <div class="collection">
      <div v-for="item in images" :key="item" class="item">
        <Item :image="item" />
      </div>
    </div>
  </div>
</template>

<script setup>
import Item from "../CollectionItems/PrimaryItem.vue";

const images = [
  {
    imageUrl: "../src/assets/collection-item-1.png",
  },
  {
    imageUrl: "../src/assets/collection-item-2.png",
  },
  {
    imageUrl: "../src/assets/collection-item-3.png",
  },
  {
    imageUrl: "../src/assets/collection-item-4.png",
  },
  {
    imageUrl: "../src/assets/collection-item-5.png",
  },
  {
    imageUrl: "../src/assets/collection-item-6.png",
  },
];
</script>

<style scoped>
@media (max-width: 320px) {
  body .container {
    max-width: 650px;
  }
}
@media (max-width: 768px) {
  body .container {
    max-width: 650px;
  }
}

.container {
  max-width: 1300px;
  margin: 15px auto;
}
.collection {
  display: flex;
  flex-wrap: wrap;
  margin: 8px 0;
}
.item {
  
  margin: 8px 0;
}
</style>