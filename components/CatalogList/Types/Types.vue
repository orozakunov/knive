<script setup>
import TagH2 from "../../TagH/TagH2.vue";
import Item from "./Item.vue";
import Dropdown from "@/components/Dropdown/Dropdown.vue";
import { ref } from "@vue/reactivity";

const dropdowns = [
  {
    label: "Новинки",
    items: [
      "Складной нож",
      "Складной нож",
      "Складной нож",
      "Складной нож",
      "Складной нож",
    ],
  },
  {
    label: "Новинки",
    items: [
      "Складной нож",
      "Складной нож",
      "Складной нож",
      "Складной нож",
      "Складной нож",
    ],
  },
  {
    label: "Новинки",
    items: [
      "Складной нож",
      "Складной нож",
      "Складной нож",
      "Складной нож",
      "Складной нож",
    ],
  },
  {
    label: "Новинки",
    items: [
      "Складной нож",
      "Складной нож",
      "Складной нож",
      "Складной нож",
      "Складной нож",
    ],
  },
];

const openDropdownIndex = ref(null)

let handleDropdownOpen = (index) => {
  if (openDropdownIndex.value === index) {
    openDropdownIndex.value = null;
  } else {
    openDropdownIndex.value = index;
  }
  console.log("test");
};
</script>

<template>
  <div class="wrapper">
    <div class="container">
      <TagH2><template v-slot:text> Ножи </template></TagH2>
      <div class="types">
        <div class="types__list">
          <Dropdown
            v-for="(dropdown, index) in dropdowns"
            :class="{ active: index === openDropdownIndex }"
            @click="handleDropdownOpen(index)"
            :key="dropdown.label"
            :label="dropdown.label"
            :items="dropdown.items"
          />
        </div>
        <div class="types__content">
          <Item />
          <Item />
          <Item />
          <Item />
          <Item />
          <Item />
         
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  margin: 0 auto;
  max-width: 1300px;
}
.wrapper {
  padding-top: 50px;
}
.types {
  display: flex;
  margin-top: 30px;
}
.types__list {
  margin-right: 20px;
  width: 580px;
}
.types__content {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 100px;
}
</style>