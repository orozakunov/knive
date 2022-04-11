<script setup>
import knive1 from "@/assets/KniveList/knive1.png";
import knive2 from "@/assets/KniveList/knive2.png";
import plusIcon from "@/assets/KniveList/pluss.svg";
import { computed } from "@vue/runtime-core";
import { useStore } from "vuex";

const store = useStore();
const cartItems = computed(() => store.state.cartItems);

const habdleClickToCart = () => {
  store.commit("ADD_KNIVE_TO_CART", knive);
  console.log(habdleClickToCart);
};

const kniveItem = [
  {
    title: "Складной нож SQ01-B",
    img: "https://tuotown.ru/wa-data/public/shop/products/54/00/54/images/172/172.300x0@2x.jpg",
    price: "850",
    new: "Новинка",
  },
  {
    title: "Складной нож JJ001-TUO-B",
    img: "https://tuotown.ru/wa-data/public/shop/products/14/00/14/images/169/169.300x0@2x.jpg",
    price: "12 850 р.",
  },
  {
    title: "Складной нож SQ01-B",
    img: "https://tuotown.ru/wa-data/public/shop/products/55/00/55/images/649/649.300x0@2x.jpg",
    price: "850",
  },
  {
    title: "Складной нож JJ001-TUO-B",
    img: "https://tuotown.ru/wa-data/public/shop/products/14/00/14/images/169/169.300x0@2x.jpg",
    price: "12 850 р.",
  },
];
</script>

<template>
  <div v-for="item in kniveItem" :key="item" class="knive-item">
    <div class="knive">
      <div class="arr">
        <img class="arr-img" :src="plusIcon" alt="" />
      </div>
      <div class="knive-div">
        <img class="knive-image" :src="knive1" alt="" />
      </div>
    </div>
    <div class="knive-desc">
      <p class="knive-p">{{ item.title }}</p>
      <span class="knive-pp">{{ item.price }} р.</span>
      <span class="knive-par">{{ item.new }}</span>
    </div>
  </div>
</template>

<style>
.knive {
  width: 240px;
  height: 410px;
  background-color: #272727;
  border-radius: 14px;
}
.knive-desc {
  font-family: "Montserrat", sans-serif;
}
.knive-item {
  padding: 0px 10px 25px 0px;
}
.knive-div {
  padding: 47px 10px 80px;
}
.knive-p {
  padding: 12px 1px;
  font-weight: 500;
  font-size: 14px;
  color: #ffffff;
}
.knive-pp {
  color: white;
  font-weight: 600;
  font-size: 14px;
  opacity: 0.5;
  margin-right: 30px;
}
.knive-par {
  font-weight: 600;
  font-size: 14px;
  color: #ff3232;
}
.arr {
  display: flex;
  justify-content: flex-end;
  padding: 35px 30px 0px 0px;
}
.arr-img:hover {
  cursor: pointer;
  background-color: #ff3232;
  border-radius: 50%;
}
@media (max-width: 768px) {
  .knive-item {
    margin: 0 20px;
  }
}
@media screen and (max-width: 376px) {
  .knive {
    width: 200px;
    height: 350px;
  }
  .knive-image {
    width: 173px;
  }
}
</style>
