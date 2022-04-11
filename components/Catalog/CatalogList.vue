<script setup>
import CatalogItem from "./CatalogItem.vue";
import Item from "./Item.vue";
import Email from "../Service/Email.vue";
import Rating from "./Rating.vue";

// const props = defineProps({
//   knives: Array,
// });
// console.log(props);
</script>

<template>
  <div class="catalog-list">
    <div class="container">
      <div class="catalog-content">
        <CatalogItem />
        <Item :knives="knives" />
      </div>
      <Email />
      <div class="catalog-list-item">
        <Item />
      </div>
      <Rating />
    </div>
  </div>
  <hr />
</template>

<style>
.catalog-list {
  padding: 90px 0 0 0;
  display: flex;
}
.catalog-content {
  display: flex;
  flex-wrap: wrap;
}
.catalog-list-item {
  padding: 50px 0;
  display: flex;
  justify-content: space-between;
}

@media (max-width: 768px) {
  .catalog-content {
    max-width: 760px;
    justify-content: center;
  }
  .catalog-list-item {
    flex-wrap: wrap;
    margin: 0 50px;
  }
  .catalog-list {
    padding: 40px 0;
    flex-wrap: wrap;
    max-width: 755px;
    justify-content: center;
    display: flex;
    flex-wrap: wrap;
  }
}
</style>
