<script setup>
// import mark from "@/assets/Basket/mark.svg";
import xIcon from "@/assets/Basket/x.svg";
import knivIcon from "@/assets/Basket/kniv-for-basket.png";
import downMark from "@/assets/Basket/mark-down.svg";
import { useStore } from "vuex";
import { computed, onMounted } from "@vue/runtime-core";

// const store = useStore();
// const knive = computed(() => store.state.knives);

// onMounted(() => {
//   store.dispatch("getKnives");
// });

const basketKnivs = [
  {
    // img: ,
    text: "Нож классного качества Knight light C653",
    count: 0,
    totalPrie: 0,
  },
  {
    // img: ,
    text: "Нож классного качества Knight light C653",
    count: 0,
    totalPrie: 0,
  },
];
</script>

<template>
  <div v-for="item in basketKnivs" :key="item" class="cart-content-div">
    <div>
      <img class="cart-content-div-img" :src="knivIcon" alt="" />
      <span class="cart-content-text">{{ item.text }}</span>
    </div>
    <div>
      <div class="cart-content-span-for-div">
        <span class="cart-content-span">{{ item.count }}</span>
        <img class="mark-down" :src="downMark" alt="" />
      </div>
      <p class="cart-price">{{ item.totalPrie }} тыс</p>
      <img :src="xIcon" alt="" />
    </div>
  </div>
  <hr />
</template>

<style>
.cart-content-div {
  align-items: center;
  display: flex;
  justify-content: space-between;
}
.cart-content-div div {
  display: flex;
  align-items: center;
}
.cart-content-div-img {
  margin: 0 30px 0 0;
}
.cart-content-div p {
  padding: 0 15px;
}
.cart-content-span {
  color: white;
  margin: 0 5px 0 5px;
}
.cart-content-span-for-div {
  border-bottom: 1px solid #adacac;
  margin: 0;
  padding-bottom: 4px;
}
.cart-content-text {
  color: white;
}
p {
  color: white;
}
hr {
  border: 1px solid #4f4f4f;
  opacity: 0.5;
}

.cart-content-div div:last-child {
  padding: 0;
}
.mark-down {
  margin: 0 10px;
}
@media (max-width: 390px) {
  .cart-content-span-for-div {
    margin: 0 5px;
  }
}
@media screen and (max-width: 376px) {
  .cart-content-text {
    font-size: 12px;
  }
  .cart-content-span-for-div {
    width: 30px;
    margin: 0 20px;
  }
  .cart-price {
    display: none;
  }
}
</style>
