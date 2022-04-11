<script setup>
import More from "./More.vue";
import MenuLogo from "./Menu-logo.vue";
import MenuSupport from "./Menu-support.vue";
</script>

<template>
  <div class="wrapper">
    <header class="header">
      <div class="container">
        <div class="header-content">
          <More />
          <MenuLogo />
          <MenuSupport />
        </div>
      </div>
    </header>
  </div>
</template>

<style scoped>
.header {
  background-color: #212121;
  font-family: "Jura", sans-serif;
}
.header-container {
  max-width: 1200px;
  margin: 0 auto;
}
.header-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 30px 0;
}
@media (max-width: 768px) {
  .header-content {
    padding: 10px;
  }
}
</style>
