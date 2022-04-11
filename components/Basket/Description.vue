<script setup></script>

<template>
  <div class="description-basket">
    <p class="description-basket-p">
      Нажимая «Выбрать способ доставки», подтверждаю, что я ознакомлен с
      условиями
      <span class="description-basket-span"
        >Публичного договора оферты и Политикой конфиденциальности,</span
      >
      а также согласен получать информационную рассылку
    </p>
    <button class="description-btn">
      <p class="description-parm">Отправить форму</p>
    </button>
  </div>
</template>

<style>
.description-basket {
  position: absolute;
  bottom: 46px;
  right: 215px;
  width: 400px;
}
.description-basket-span {
  cursor: pointer;
  font-weight: 400;
  font-size: 14px;
  color: #ed0c0c;
}
.description-basket-p {
  font-weight: 400;
  font-size: 14px;
  color: #adacac;
}
.description-btn {
  cursor: pointer;
  padding: 16px 34px;
  background: #c80000;
  border-radius: 27px;
  border: none;
  margin: 35px auto;
}

.description-btn p {
  color: white;
}
@media (max-width: 768px) {
  .description-basket {
    position: absolute;
    bottom: 145px;
    right: 30px;
    width: 295px;
  }
}
@media screen and (max-width: 376px) {
  .description-basket {
    bottom: 0;
  }
  .description-basket-p {
    font-style: normal;
    font-weight: 400;
    font-size: 11px;
    text-align: center;
  }
  .description-btn {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 10px;
  }
  .description-parm {
    font-size: 12px;
  }
}
</style>
