<script setup>
import kniveBigIcom from "@/assets/KniveList/kniveBig.png";
import arrow from "@/assets/arrow.svg";
import router from "../../router";

const handleClick = () => {
  router.push("/product");
};
</script>

<template>
  <div @click="handleClick" class="catalog-item">
    <img class="catalog-item-img" :src="kniveBigIcom" alt="" />
    <div class="catalog-item-div">
      <h4 class="catalog-item-h4">Познакомьтесь с коллекцией ножей TUOTOWN</h4>
      <img class="catalog-item-arr" :src="arrow" alt="" />
    </div>
  </div>
</template>

<style>
.catalog-item {
  padding: 0 10px 0 0;
  position: relative;
  cursor: pointer;
  font-family: "Montserrat", sans-serif;
}
.catalog-item-img {
  width: 590px;
  height: 480px;
}
.catalog-item-h4 {
  color: white;
  font-weight: 600;
  font-size: 17px;
  color: #ffffff;
}
.catalog-item-div {
  display: flex;
  position: absolute;
  bottom: 65px;
  padding: 0 25px;
}
.catalog-item-arr {
  margin: 0 0 0 80px;
}
@media (max-width: 768px) {
  .catalog-item {
    margin: 20px auto;
  }
}
@media (max-width: 390px) {
  .catalog-item-img {
    width: 345px;
    height: 267px;
  }
  .catalog-item-div {
    bottom: 20px;
  }
}
@media screen and (max-width: 376px) {
  .catalog-item-img {
    width: 290px;
    height: 290px;
  }
  .catalog-item-div {
    bottom: 30px;
  }
  .catalog-item-h4 {
    font-size: 14px;
  }
}
</style>
