<script setup>
import KnivsVue from "./Knivs.vue";

import AllKnivsMeatIcon from "@/assets/AllKnivsIcon/AllKnivsMeat.png";
import AllKnivsIcon from "@/assets/AllKnivsIcon/AllKnivs.png";
import AllKnivsIcon2 from "@/assets/AllKnivsIcon/AllKnivs2.png";

const knivs = [
  {
    id: 1,
    date: "4 августа 2021 12:24",
    img: "https://tuotown.ru/wa-data/public/site/img/pic_news4.jpg",
    content: "Традиционные виды японских кухонных ножей",
  },
  {
    id: 2,
    date: "10 июля 2021 17:23",
    img: "https://tuotown.ru/wa-data/public/site/img/pic_news3.jpg",
    content: "Как ухаживать за японскими кухонными ножами?",
  },
  {
    id: 3,
    date: "20 августа 2021 21:12",
    img: "https://tuotown.ru/wa-data/public/site/img/pic_news2.jpg",
    content: "Всемирная история режущих клинков — взгляд в прошлое",
  },
];
</script>

<template>
  <div class="all-knivs">
    <div class="container">
      <div class="all-knivs-content">
        <h1>Всё самое интересное о ножах</h1>
        <div class="all-knivs-content-div">
          <div v-for="item in knivs" :key="item">
            <div class="all-knivs-span">
              <span class="all-knivs-spann">{{ item.date }}</span>
            </div>
            <a href="#">
              <router-link to="/product">
                <img :src="item.img" alt=""
              /></router-link>
            </a>
            <div class="all-knivs-p">
              <p class="all-knivs-pr">
                {{ item.content }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.all-knivs {
  padding: 60px 0 40px;
}
h1 {
  font-family: "Jura", sans-serif;
  color: white;
  font-weight: 500;
  font-size: 35px;
  margin-bottom: 40px;
}
.about-knivs {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.all-knivs-content-div {
  display: flex;
}
.all-knivs-content-div img {
  width: 350px;
  height: 420px;
}
.all-knivs-content div {
  font-family: "Montserrat", sans-serif;
  position: relative;
  padding: 0 20px;
}
.all-knivs-content div:first-child {
  padding: 0;
}
.all-knivs-content div:last-child {
  padding: 0;
}
.all-knivs-pr {
  position: absolute;
  padding: 0 35px 22px;
  top: -100px;
  left: 17px;
  font-weight: 500;
  font-size: 17px;
  color: #ffffff;
}
.all-knivs-span {
  position: absolute;
  bottom: -53px;
  font-weight: 400;
  font-size: 14px;
  color: #ffffff;
}
.all-knivs-spann {
  padding-left: 200px;
}

.all-knivs-p::before {
  content: "";
  background: #c80000;
  border-radius: 0px 0px 14px 14px;
  width: 380px;
  height: 83px;
}
/* .all-knivs-pr:hover {
  height: 75px;
  background: #c80000;
  border-radius: 0px 10px 24px 14px;
} */

/* @media (max-width: 1024px) {
  .all-knivs {
    display: flex;
    width: 610px;
    padding: 36px 221px;
  }
  .all-knivs-content {
    flex-wrap: wrap;
    padding: 0 50px;
  }
  .all-knivs-content div {
    padding: 0;
  }
} */

@media (max-width: 768px) {
  .all-knivs-content {
    padding: 0 75px;
  }
  .all-knivs-content div {
    padding: 0;
    flex-direction: column;
  }
  .all-knivs-content-div img {
    width: 583px;
    height: 303px;
  }

  .all-knivs-spann {
    padding-left: 400px;
  }
  .all-knivs-pr {
    position: absolute;
    padding-top: 40px;
    top: -100px;
    left: 17px;
    font-weight: 500;
    font-size: 17px;
    color: #ffffff;
  }
}

@media screen and (max-width: 376px) {
  .all-knivs {
    display: none;
  }
}
</style>
