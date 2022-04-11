<script setup></script>

<template>
  <div class="total-price">
    <div class="total-price-content">
      <label>К оплате:</label>
      <span class="total-price-span">747,9 тыс.р.</span>
    </div>
  </div>
</template>

<style>
.total-price {
  border-radius: 0 0 20px 20px;
  background-color: #232323;
  padding: 20px 25px;
}
.total-price-content {
  flex-direction: column;
  display: flex;
  align-items: flex-end;
}
label {
  color: #adacac;
}
.total-price-span {
  color: white;
}
</style>
