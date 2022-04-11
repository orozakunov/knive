<script setup>
import Title from "./Title.vue";
import Description from "./Description.vue";
</script>

<template>
  <div class="descrioption">
    <div class="container">
      <Title />
      <Description />
    </div>
  </div>
</template>

<style>
.descrioption {
  padding: 40px 0;
}

@media screen and (max-width: 376px) {
  .descrioption {
    display: none;
  }
}
</style>
