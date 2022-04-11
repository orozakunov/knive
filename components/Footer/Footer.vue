<script setup>
import Description from "./Description.vue";
import Information from "./information.vue";
import ContactInfarmation from "./ContactInfarmation.vue";
import Support from "./Support.vue";
</script>

<template>
  <div class="wrapper">
    <footer class="footer">
      <div class="container">
        <div class="content">
          <Description />
          <Information />
          <ContactInfarmation />
        </div>
      </div>
      <Support />
    </footer>
  </div>
</template>

<style>
.footer {
  font-family: "Jura", sans-serif;
  background-color: #272727;
  margin-top: 40px;
}
.content {
  display: flex;
  justify-content: space-between;
  padding: 45px 0;
}

@media (max-width: 768px) {
  .content {
    display: block;
  }
}
</style>
