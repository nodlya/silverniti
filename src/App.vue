<template>
  <div class="page-wrapper">
    <nav-bar />
    <div class="content">
      <main-page />
      <partners-content id="partners"/>
      <v-accordeon id="links" />
    </div>
    <footer-component id="footer"/>
  </div>
</template>

<script>
import MainPage from "./components/MainPage.vue";
import NavBar from "./components/NavBar.vue";
import FooterComponent from "./components/FooterComponent.vue";
import VAccordeon from "./components/VAccordeon.vue";
import PartnersContent from "./components/PartnersContent.vue";

export default {
  name: "App",
  components: {
    MainPage,
    NavBar,
    FooterComponent,
    VAccordeon,
    PartnersContent
  }
};
</script>

<style>
@font-face {
  font-family: "Manrope";
  font-weight: 400;
  src: url(./assets/fonts/Manrope.ttf);
}

/* semiBold шрифт */
@font-face {
  font-family: "Manrope";
  font-weight: 600;
  src: url(./assets/fonts/Manrope.ttf);
}

* {
  font-family: "manrope";
}

nav-bar {
  z-index: 1 !important;
}

.page-wrapper {
  display: flex;
  flex-direction: column;
  gap: 130px;
}

.content {
  margin-top: 130px;
  display: flex;
  flex-direction: column;
  gap: 100px;
  color: black;
  padding: 0 40px;
}
</style>
