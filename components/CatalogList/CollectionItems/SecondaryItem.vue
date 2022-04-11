<template>
  <div class="collection__secondary-item">
    <img :src="image.imageUrl" />
    <span>Ножи с покрытием</span>
  </div>
</template>

<script setup>
defineProps({
  image: Object,
});
</script>

<style scoped>
.collection__secondary-item {
  position: relative;
  height: 100%;
  width: 100%;
  margin: 0 5px;
}
.collection__secondary-item img {
  width: 100%;
}
.collection__secondary-item span {
  font-family: "Montserrat";
  font-style: normal;
  font-weight: 600;
  font-size: 13px;
  line-height: 20px;
  display: flex;
  align-items: center;
  text-align: center;
  color: #ffffff;
  width: 100%;
  height: 100%;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  background: rgba(0, 0, 0, 0.6);
  border-radius: 15px;
}
</style>