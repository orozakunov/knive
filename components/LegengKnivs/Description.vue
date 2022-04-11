<script setup>
import MeatIcon2 from "@/assets/meat2.png";
</script>

<template>
  <div class="desc">
    <div class="desc-content">
      <p>
        Истинная красота ножа — совершённая функциональность и визуальная
        гармония. Этот предмет издревле сопутствовал человеку: от зари
        цивилизации до сегодняшних дней. На протяжении всей истории человечества
        он был верным помощником, незаменимым инструментом и грозным оружием.
        Предлагаем изделия Hi-end качества по доступным ценам настоящим
        ценителям японских ножей.
      </p>
      <p>
        Отличительной чертой нашего интернет-магазина являются уникальные
        торговые предложения, эксклюзивность продукции, неизменно высокое
        качество и выгодные цены. Осуществляем продажи элитных японских кухонных
        ножей для профессионалов и любителей. В обширной ассортиментной линейке
        представлены изделия для различных потребностей и любого бюджета —
        от столовых приборов до шеф-ножей.
      </p>
      <span>
        Ножи «Tuotown» – это главный инструмент поваров и секрет кулинарного
        мастерства
      </span>
    </div>
    <div>
      <img :src="MeatIcon2" alt="" />
    </div>
  </div>
  <div class="hr"></div>
</template>

<style>
.desc {
  padding: 40px 0 0 0;
  justify-content: space-between;
  display: flex;
}
.desc-content {
  padding: 0 79px 40px 0;
}
.desc div {
  max-width: 810px;
}
.desc p {
  font-family: "Montserrat", sans-serif;
  color: white;
  font-weight: 400;
  font-size: 16px;
  margin-bottom: 40px;
}
.desc span {
  color: white;
  font-weight: 600;
  font-family: "Jura", sans-serif;
  font-size: 28px;
}
.hr {
  margin-top: 60px;
  opacity: 0.1;
  border: 1px solid #ffffff;
}

@media (max-width: 390px) {
  .desc {
    display: none;
  }
}
@media (max-width: 768px) {
  .desc {
    width: 670px;
    padding: 0 50px 0;
  }
  .desc-content {
    padding: 0 30px;
  }
  .hr {
    display: none;
  }
}
</style>
