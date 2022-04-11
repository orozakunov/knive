<script setup>
import MeatIcon from "@/assets/meat.png";
</script>

<template>
  <div class="title">
    <div>
      <img class="title-img" :src="MeatIcon" alt="" />
    </div>
    <div class="subtitle">
      <div>
        <h1>«Tuotown» – легендарные ножи, создающие шедевры</h1>
        <p>
          Компания «Tuotown» – эксклюзивный представитель профессиональных
          кухонных ножей, изготовленных лучшими мастерами Восточной Азии с
          применением передового европейского оборудования и современных
          материалов. Они отличаются идеальным балансом и фантастической
          остротой. Сочетают в себе вековые традиции и новейшие разработки.
          Также предлагаем широкий ассортимент сопутствующих товаров.
        </p>
      </div>
    </div>
  </div>
</template>

<style>
.title {
  display: flex;
  background-color: #373737;
}
.subtitle {
  padding: 0 80px;
}
.subtitle h1 {
  font-family: "Jura", sans-serif;
  font-weight: 500;
  font-size: 35px;
  margin-bottom: 50px;
  color: white;
}
.subtitle p {
  font-family: "Montserrat", sans-serif;
  color: white;
  font-weight: 400;
  font-size: 16px;
}

@media (max-width: 375px) {
  .title {
    display: block;
    padding: 50px 32px;
  }
  .subtitle {
    padding: 20px 0;
    width: 300px;
  }
}
@media (max-width: 768px) {
  .title {
    padding: 133px 70px;
  }
}

@media (max-width: 390px) {
  .subtitle {
    padding: 0;
    margin: 0 5px;
  }
  .title {
    flex-direction: column;
    box-sizing: border-box;
    padding: 1px 1px;
    margin: 0 20px;
  }
  .title-img {
    width: 250px;
    height: 250px;
  }
}
</style>
