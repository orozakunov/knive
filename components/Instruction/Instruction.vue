<script setup>
import { ref } from "@vue/reactivity";

const showDescription = ref(false);

const showDesc = () => {
  showDescription.value = !showDescription.value;
};
</script>

<template>
  <h1 class="instruction-h1">Инструкция</h1>
  <div class="instruction-content">
    <h1 class="title">
      Безопасность при работе ножами - основное правило на кухне
    </h1>
    <p class="instruction-desc">
      Будьте предельно осторожны в обращении с кухонными ножами! Не соблюдение
      правил использования кухонных ножей, является самой распространенной
      причиной несчастных случаев. Соблюдение перечисленных ниже пунктов –
      поможет избежать неприятных моментов и обеспечит больший уровень
      безопасности:
    </p>
    <button @click="showDesc" class="next">Подробнее</button>
    <router-link to="/service">
      <button class="toHome">Назад</button>
    </router-link>
    <div v-if="showDescription">
      <h1>Важно!</h1>
      <p class="instruction-description">
        перед использованием кухонного ножа – расчистите рабочую поверхность
        всегда использовать разделочную доску (чтобы избежать скольжения доски
        по поверхности разделочного стола, нужно подложить под нее влажное
        полотенце или резиновый коврик) не работать с ножом в направлении своего
        тела, крепко держать рукоять не держать в руке нож и при этом заниматься
        чем-то отвлекающим использовать хорошо заточенные ножи следить, чтобы
        руки и рукоять ножа были сухими, (большинство порезов происходит из-за
        соскальзывания ножа с разрезаемого продукта на палец или на руку)
        передавать нож кому-либо нужно ручкой вперед не размахивать ножом не
        класть нож режущей кромкой вверх не вкалывать нож в продукты или в
        разделочный стол не пытаться поймать падающий нож не допустимо
        использовать кухонный нож не по назначению, нельзя резать замороженное
        мясо и кости – режущая кромка высокой твердости может быть повреждена, а
        при больших поперечных нагрузках на клинок возможно обламывание лезвия
        не мыть режущую кромку ножа голыми руками (только с применением губки)
        мыть нож после каждого применения; в зависимости от типа стали протирать
        насухо, окисляющиеся (ржавеющие) лезвия рекомендуем протирать ромашковым
        маслом затачивать и править ножи в соответствии с их характеристиками
        (многослойные ножи нельзя точить керамическими точилками) точить и
        править следует только чистые ножи не проверяйте остроту ножа пальцем
        хранить ножи, отдельно от других приборов не позволять детям играть с
        кухонными ножами. Помните, что ножи из Японии это своего рода
        произведение искусства, и при адекватном обращении способны безупречно
        служить на Вашей кухне долгие годы и доставлять Вам немало удовольствия
        при приготовлении пищи.
      </p>
      <iframe
        width="560"
        height="315"
        src="https://www.youtube.com/embed/mqSHK67-_9U"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
    </div>
  </div>
</template>

<style scoped>
.instruction-content {
  padding: 0 0 40px 0;
  align-items: center;
  justify-content: center;
}
.instruction-h1 {
  text-align: center;
  margin-top: 40px;
}
.instruction-desc {
  max-width: 550px;
  margin: 40px 0;
}
.instruction-description {
  margin: 40px 0;
}
.next {
  margin: 0 20px 20px 0;
}
.next:hover {
  background-color: #c80000;
}
.toHome:hover {
  background-color: #c80000;
}
@media (max-width: 768px) {
  .title {
    width: 300px;
    padding: 0;
  }
  .instruction-content {
    margin: 0 40px;
  }
}
</style>
