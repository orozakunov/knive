<script setup>
import CertificateIcon1 from "@/assets/Certificate/Certificate1.png";
import CertificateIcon2 from "@/assets/Certificate/Certificate2.png";
import CertificateIcon3 from "@/assets/Certificate/Certificate3.png";
import { useRouter } from "vue-router";

const router = useRouter();

const handleClick = () => {
  router.push("/service");
};
</script>

<template>
  <h1 class="certificate-h1">Сертификаты</h1>
  <div class="certificate-content">
    <img :src="CertificateIcon1" alt="" />
    <img :src="CertificateIcon2" alt="" />
    <img :src="CertificateIcon3" alt="" />
  </div>
  <div>
    <button class="certificate-bnt" @click="handleClick">Назад</button>
  </div>
</template>

<style scoped>
.certificate-content {
  display: flex;
  justify-content: space-between;
  padding: 0 0 40px 0;
  border-radius: 20px;
  /* background-color: #c4c4c4; */
}
.certificate-h1 {
  text-align: center;
  margin-top: 40px;
}
img {
  width: 350px;
  height: 400px;
}
div {
  display: flex;
  align-items: center;
  justify-content: center;
}
.certificate-bnt:hover {
  background-color: #c80000;
}
@media (max-width: 768px) {
  .certificate-content {
    flex-direction: column;
  }
  img {
    margin: 20px 0;
  }
}
</style>
