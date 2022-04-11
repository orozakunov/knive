<template>
  <div class="collection-item">
    <img :src="image.imageUrl" />
    <span>Познакомьтесь с коллекцией ножей TUOTOWN</span>
  </div>
</template>

<script setup>
defineProps({
  image: Object,
});
</script>

<style scoped>
@media (max-width: 768px) {
    body .collection-item img {
        width: 50%;
    }
}

.collection-item {
  position: relative;
  margin: 0 8px;
}
.collection-item::before {
  content: "";
  position: absolute;
  bottom: 27px;
  right: 20px;
  width: 15px;
  height: 7px;
  background: url(../src/assets/arrow.svg) no-repeat center;
}
.collection-item span {
  position: absolute;
  bottom: 20px;
  left: 20px;
  font-family: "Montserrat";
  font-style: normal;
  font-weight: 600;
  font-size: 11px;
  line-height: 20px;
  color: #ffffff;
}
.collection-item img {
  width: 100%;
  height: 100%;
}
</style>