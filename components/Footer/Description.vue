<script setup>
import LogoIсon from "@/assets/Social/logo.svg";
</script>

<template>
  <div class="description">
    <div class="logo">
      <router-link class="logo-img" to="/">
        <img class="logo-img" :src="LogoIсon" alt="" />
      </router-link>
      <p class="logo-p">легендарные ножи, создающие шедевры</p>
    </div>
    <p class="description-p">
      Компания «Tuotown» – эксклюзивный представитель профессиональных кухонных
      ножей, изготовленных лучшими мастерами Восточной Азии с применением
      передового европейского оборудования и современных материалов.
    </p>
    <p class="description-p">
      Они отличаются идеальным балансом и фантастической остротой. Сочетают
      в себе вековые традиции и новейшие разработки. Также предлагаем широкий
      ассортимент сопутствующих товаров.
    </p>
  </div>
</template>

<style>
.logo-p {
  color: white;
  padding: 0 25px;
}
.logo {
  display: flex;
}
.description-p {
  padding: 20px 0;
  color: white;
  opacity: 0.5;
  max-width: 365px;
}

@media (max-width: 768px) {
  .logo {
    max-width: 400px;
  }
  .logo-a {
    padding: 0;
    margin: 0;
  }
}
@media screen and (max-width: 376px) {
  .information {
    padding: 0;
    max-width: 342px;
    box-sizing: border-box;
  }
  .information-h3 {
    max-width: 100px;
  }
  .informationList {
    max-width: 300px;
  }
}
</style>
