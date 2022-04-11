<script setup>
import toggle from "@/assets/Basket/toggle.svg";
import { ref } from "@vue/reactivity";
import { onMounted } from "vue";

const currentSlide = ref(1);
const getSlideCount = ref(null);
const autoPlayEnabled = ref(true);
const timeoutDuration = ref(5000);

//nex slide

const nextSlide = () => {
  if (currentSlide.value === getSlideCount.value) {
    currentSlide.value = 1;
    return;
  }
  currentSlide.value += 1;
};

// prev slide
const prevSlide = () => {
  if (currentSlide.value === 1) {
    currentSlide.value = 1;
    return;
  }
  currentSlide.value -= 1;
};
// go to slide by just pressing the needed button
const goToSlide = (index) => {
  currentSlide.value = index + 1;
};
// autoplay
const autoplay = () => {
  setInterval(() => {
    nextSlide();
  }, timeoutDuration.value);
};
if (autoPlayEnabled.value) {
  autoplay();
}
onMounted(() => {
  getSlideCount.value = document.querySelectorAll(".slide").length;
});
</script>

<template>
  <div class="carousel">
    <slot :currentSlide="currentSlide" />

    <!-- Navigation -->
    <div class="navigationbox">
      <div class="navigate">
        <div class="toggle-left">
          <img @click="prevSlide" :src="toggle" alt="" />
        </div>
        <div class="pagination">
          <span
            @click="goToSlide(index)"
            v-for="(slide, index) in getSlideCount"
            :key="index"
            :class="{ active: index + 1 === currentSlide }"
          >
            {{ slide }}
          </span>
        </div>
        <div class="toggle-right">
          <img @click="nextSlide" :src="toggle" alt="" />
        </div>
      </div>

      <!-- Slider Title -->
      <div class="title">
        <h1>Исключительное качество без компромиссов</h1>
        <p>
          Ножи «Tuotown» – это главный инструмент поваров и секрет кулинарного
          мастерства
        </p>
        <div>
          <router-link to="/product">
            <button class="carousel-btn">
              <span class="link">ПОДРОБНЕЕ</span>
            </button>
          </router-link>
        </div>
      </div>
    </div>

    <!-- Pagination -->
  </div>
</template>

<style scoped>
.navigate {
  position: absolute;
  display: flex;
  justify-content: space-between;
  width: 100%;
  bottom: 30px;
}
.navigationbox {
  position: relative;
  bottom: 30px;
  height: 100%;
  width: 90%;
  margin: 0 auto;
  align-items: center;
  text-align: center;
}
.toggle-right {
  transform: rotate(180deg);
  cursor: pointer;
}
.toggle-left {
  cursor: pointer;
}
/* styles of navigation */
.pagination {
  position: absolute;
  bottom: 24px;
  width: 100%;
  display: flex;
  gap: 26px;
  justify-content: center;
  align-items: center;
}
span {
  color: beige;
  cursor: pointer;
  width: 20px;
  border-radius: 50%;
  box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
}

.active {
  background-color: white;
}
/* styles of pagination */
.title {
  display: flex;
  flex-direction: column;
  background: none;
  max-width: 600px;
  text-align: initial;
  position: absolute;
  top: 80px;
  left: 70px;
}
h1 {
  font-family: "Jura";
  font-style: normal;
  font-weight: 400;
  font-size: 41px;
  line-height: 48px;
  color: #ffffff;
  margin-bottom: 25px;
}
p {
  font-family: "Montserrat";
  font-style: normal;
  font-weight: 400;
  font-size: 19px;
  line-height: 23px;
  color: #ffffff;
}
button {
  font-weight: 600;
  font-size: 14px;
  color: #ffffff;
  cursor: pointer;
  margin-top: 40px;
  width: 165px;
}
.carousel-btn {
  border: 2px solid #c80000;
  background: none;
  padding: 16px 35px;
  border-radius: 40px;
}
button:hover {
  transition: 0.9;
  background-color: #c80000;
  color: #444444;
}
.link {
  color: white;
}

@media (max-width: 768px) {
  .title {
    padding: 20px 0;
  }
  .navigate {
    bottom: 115px;
  }
}

@media (max-width: 390px) {
  .navigate {
    display: none;
  }

  .title {
    top: 100px;
    padding: 0;
    left: 0;
  }
}

@media screen and (max-width: 376px) {
  .navigate {
    display: none;
  }
  .title {
    font-family: "Jura";
    font-style: normal;
    font-weight: 500;
    font-size: 24px;
    margin: -65px;
    box-sizing: border-box;
    max-width: 342px;
    top: 125px;
    left: 80px;
  }
}
h1 {
  font-style: normal;
  font-weight: 500;
  font-size: 21px;
}
p {
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  max-width: 370px;
}
.carousel-btn {
  padding: 10px;
}
</style>
