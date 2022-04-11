<script setup>
import contentItem from "@/assets/types-content-item.jpg";
</script>

<template>
  <div class="types__content-item">
    <div class="types__content-frame">
      <img :src="contentItem" alt="" />
    </div>
    <div class="types__content-title">
      <h4>Складной нож SQ01-B</h4>
      <p>850 р.</p>
      <span>Новинка</span>
    </div>
  </div>
</template>

<style scoped>
.types__content-item {
  margin: 0 15px;
}
.types__content-frame {
  position: relative;
  width: 300px;
  height: 460px;
  border-radius: 14px;
  background-color: #272727;
}
.types__content-frame img {
  display: block;
  margin: auto;
  padding-top: 120px;
}
.types__content-frame::before {
  content: "";
  position: absolute;
  top: 25px;
  right: 25px;
  width: 24px;
  height: 24px;
  background: url("../src/assets/plus-sign.svg") no-repeat center;
}
.types__content-title h4 {
  font-family: "Montserrat";
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 28px;
  color: #ffffff;
  margin-top: 15px;
}
.types__content-title p {
  display: inline-block;
  padding: 0 25px 30px 0;
  font-family: "Montserrat";
  font-style: normal;
  font-weight: 600;
  font-size: 14px;
  line-height: 28px;
  color: #ffffff;
  opacity: 0.5;
}
.types__content-title span {
  font-family: "Montserrat";
  font-style: normal;
  font-weight: 600;
  font-size: 14px;
  line-height: 28px;
  color: #ff3232;
}
</style>