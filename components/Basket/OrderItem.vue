<script setup>
import { ref } from "@vue/reactivity";

const recipient = ref("");
const email = ref("");
const number = ref("");
console.log(recipient.value, email.value, number.value);
</script>

<template>
  <div class="order-item">
    <div class="order-wrapper">
      <p class="order-p">Получатель</p>
      <input
        v-model="recipient"
        type="text"
        placeholder="Имя Фамилия"
        class="order-input"
      />
      <svg
        width="299"
        height="2"
        viewBox="0 0 299 2"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M298.699 2L0.201172 1.99997L0.201172 0L298.699 2.60955e-05L298.699 2Z"
          fill="#828282"
        />
      </svg>
    </div>
  </div>
  <div class="order-item">
    <div class="order-wrapper">
      <p class="order-p">E-mail</p>
      <input
        v-model="email"
        type="text"
        placeholder="Ваша почта"
        class="order-input"
      />
      <svg
        width="299"
        height="2"
        viewBox="0 0 299 2"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M298.699 2L0.201172 1.99997L0.201172 0L298.699 2.60955e-05L298.699 2Z"
          fill="#828282"
        />
      </svg>
    </div>
  </div>
  <div class="order-item">
    <div class="order-wrapper">
      <p class="order-p">Мобильный телефон</p>
      <input
        v-model="number"
        type="text"
        placeholder="+7 (___) ___-__-__"
        class="order-input"
      />
      <svg
        width="299"
        height="2"
        viewBox="0 0 299 2"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M298.699 2L0.201172 1.99997L0.201172 0L298.699 2.60955e-05L298.699 2Z"
          fill="#828282"
        />
      </svg>
    </div>
  </div>
</template>

<style>
.order-item {
  display: flex;
  width: 332px;
  padding: 15px 18px;
  margin: 30px 0;
  flex-direction: column;
  border-radius: 5px;
  background-color: #303030;
}
.order-wrapper {
  padding: 15px 20px;
}
.order-p {
  margin-bottom: 10px;
  font-weight: 500;
  font-size: 12px;
  color: #828282;
  opacity: 0.87;
}
.order-input {
  background-color: #303030;
  color: white;
}

@media screen and (max-width: 376px) {
 .order-item {
   padding: 0;
 }
}
</style>
