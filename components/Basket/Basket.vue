<script setup>
import Cart from "./Cart.vue";
import TotalPrice from "./TotalPrice.vue";
import Natification from "./Natification.vue";
import Order from "./Order.vue";
import Email from "@/components/Service/Email.vue";

import { ref } from "@vue/reactivity";

const showCart = ref(false);

const showCarts = () => {
  showCart.value = !showCart.value;
};
</script>

<template>
  <div v-if="showCart">
    <Cart />
    <TotalPrice />
  </div>
  <div v-else>
    <div class="empty">
      <h1>Ваша Корзина пуста</h1>
    </div>
  </div>
  <div @click="showCarts">
    <Natification />
  </div>
  <Order />
  <Email />
</template>

<style>
.empty {
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 100px 0;
}
</style>
