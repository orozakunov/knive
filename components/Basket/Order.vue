<script setup>
import OrderItem from "./OrderItem.vue";
import Description from "./Description.vue";
</script>

<template>
  <div class="order">
    <div class="order-content">
      <h1 class="order-h1">
        Для подтверждения заказа - введите ваши данные и мы перезвоним вам
      </h1>
      <OrderItem />
      <Description />
    </div>
    <!-- <div class="empty">
      <p>Ваша корзина пуста</p>
    </div> -->
  </div>
</template>

<style>
.order {
  background-color: #232323;
}
.order-content {
  position: relative;
  padding: 60px 40px;
}
.order-h1 {
  max-width: 790px;
}
@media (max-width: 390px) {
  .order-content {
    padding: 20px 10px 230px;
  }
  .description-basket {
    bottom: 5px;
  }
  .description-basket-p {
    text-align: center;
  }
  .description-btn {
    display: flex;
    align-items: center;
    justify-content: center;
  }
}
@media screen and (max-width: 376px) {
  .order-h1 {
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
  }
  .order-content {
    padding: 45px 125px 190px 20px;
  }
}
</style>
