<script setup>
import Item from "./Item.vue";
import Description from "./Description.vue";

import MoreIcon from "@/assets/Menu/more.svg";
import bacgroundIcon from "@/assets/Menu/menu-background.png";
import LocationIcon from "@/assets/Menu/location.svg";

import { ref } from "@vue/reactivity";
import { onMounted } from "@vue/runtime-core";

const menuBar = ref(false);
const menuRef = ref(null);

const handleClickBar = () => {
  menuBar.value = !menuBar.value;
};

onMounted(() => {
  document.addEventListener("click", (event) => {
    if (!event.path.includes(menuRef.value)) {
      menuBar.value = false;
    }
  });
});
</script>
<template>
  <div ref="menuRef" class="menu-wrapper">
    <div v-if="menuBar" class="menu">
      <img class="menu-img" :src="bacgroundIcon" alt="" />
      <div @click="handleClickBar" class="menu-content">
        <svg
          class="menu-svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M15 18L9 12L15 6"
            stroke="white"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
        <div>
          <Item />
          <Description />
        </div>
      </div>
    </div>
    <div class="menu-more">
      <div class="burger" @click="handleClickBar">
        <img :src="MoreIcon" alt="" />
      </div>
      <router-link to="/map">
        <img class="more-img" :src="LocationIcon" alt="" />
      </router-link>
      <a class="more-a" href="tel:8 981 120-11-17">8 981 120-11-17</a>
    </div>
  </div>
</template>

<style>
.menu-more {
  display: flex;
  align-items: center;
}
.more-img {
  margin: 0 30px;
}
.more-a {
  font-weight: 500;
  font-family: "Montserrat", sans-serif;
  font-size: 20px;
  color: white;
  list-style: none;
  text-decoration: none;
}
.menu {
  z-index: 1;
  position: relative;
  position: absolute;
  top: 0;
  left: 0;
  transition: 0.4s;
}
.menu-svg {
  position: absolute;
  top: 20px;
  left: 30px;
}
.menu-img {
  transition: 0.4s;
  width: 440px;
  height: 700px;
}
.burger {
  cursor: pointer;
}
.more-img {
  cursor: pointer;
}
@media (max-width: 768px) {
  .menu-img {
    max-width: 315px;
  }
}

@media screen and (max-width: 376px) {
  .more-a {
    display: none;
  }
  .menu-img {
    max-width: 245px;
  }
}
</style>
