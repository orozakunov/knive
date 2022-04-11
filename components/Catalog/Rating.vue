<script setup>
import Item from "./Item.vue";
</script>

<template>
  <div class="rating">
    <div class="rating-h4">
      <h4 class="rating-pop">НОВИНКИ</h4>
      <h4 class="rating-pop">ПОПУЛЯРНОЕ</h4>
    </div>
    <div class="rating-content">
      <Item />
    </div>
  </div>
</template>

<style>
.rating-h4 {
  font-family: "Montserrat", sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
}
/* .rating-h4 h4 {
  margin: 30px 30px; */
/* } */
.rating-content {
  display: flex;
  justify-content: space-between;
}
.rating-pop {
  position: relative;
  justify-content: space-between;
  margin: 20px 20px;
}
.rating-h4::before {
  content: "";
  position: absolute;
  width: 100%;
  bottom: 0;
  left: 0;
}
.rating-h4:hover::before {
  content: "";
  position: absolute;
  width: 100%;
  bottom: 0;
  left: 0;
  border-bottom: 2px solid #c80000;
}
@media (max-width: 768px) {
  .rating {
    display: none;
  }
}
</style>
