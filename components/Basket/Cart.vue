<script setup>
import AddKnivVue from "./AddKniv.vue";
import backIcon from "@/assets/Basket/back.svg";
</script>

<template>
  <div class="cart">
    <div class="cart-item">
      <div class="back">
        <div>
          <img :src="backIcon" alt="" />
          <router-link class="cart-router" to="/">
            <span class="cart-item-back">К покупкам</span>
          </router-link>
        </div>
        <h1 class="cart-item-h1">Корзина</h1>
      </div>
      <div class="cart-content">
        <div>
          <AddKnivVue />
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.cart {
  padding: 40px 0 0 0;
}
.cart-item-h1 {
  text-align: center;
}
.cart-content {
  border-radius: 20px 20px 0 0;
  background-color: #303030;
  padding: 20px 25px 0 25px;
}
.cart-item-back {
  font-weight: 400;
  font-size: 14px;
  color: #adacac;
}
.back div {
  cursor: pointer;
}
.back img {
  margin: 0 10px;
}
.cart-router {
  list-style: none;
  text-decoration: none;
}
@media screen and (max-width: 376px) {
  .cart-item-back {
    display: none;
  }
}
</style>
