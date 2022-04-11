<script setup>
import locationIcon from "@/assets/Natification/location.png";
import paymantIcon from "@/assets/Natification/payment.png";

// const items = [
//   {
//     title: "Доставка",
//     content: "Саратов, 25.10 бесплатно",
//   },
//   {
//     title: "Оплата",
//     content: "Самый удобный для Вас: Картой на сайте",
//   },
// ];
</script>

<template>
  <div class="natification">
    <div class="natification-item">
      <img :src="locationIcon" alt="" />
      <div>
        <span class="natification-span">Доставка</span>
        <p>Саратов, 25.10 бесплатно</p>
      </div>
    </div>
    <div class="natification-item">
      <img :src="paymantIcon" alt="" />
      <div>
        <span class="natification-span">Оплата</span>
        <p>Самый удобный для Вас: Картой на сайте</p>
      </div>
    </div>
  </div>
</template>

<style>
.natification {
  display: flex;
  width: 740px;
  justify-content: space-between;
}
.natification-item {
  position: relative;
  display: flex;
  padding: 30px 0;
  align-items: center;
}
.natification-item div {
  padding: 0 15px;
}
.natification-span {
  color: white;
}
.natification-item::before {
  content: "";
  position: absolute;
  width: 83px;
  left: 95px;
  top: 67px;
  border-bottom: 2px solid #ed0c0c;
}
.natification-item p {
  margin-top: 8px;
  font-weight: 500;
  font-size: 14px;
  color: #adacac;
}
@media screen and (max-width: 376px) {
  .natification {
    flex-direction: column;
  }
  .natification-item {
    max-width: 355px;
  }
}
</style>
