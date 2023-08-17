<template>
  <div>
    <nav-bar />
    <main-page />
    <img
      src="./assets/Line 4.png"
      class="line"
    />
    <v-accordeon title="Вконтакте"></v-accordeon>

    <footer-component />
  </div>
</template>

<script>
import MainPage from "./components/MainPage.vue";
import NavBar from "./components/NavBar.vue";
import FooterComponent from "./components/FooterComponent.vue";
import VAccordeon from "./components/VAccordeon.vue";

export default {
  name: "App",
  components: {
    MainPage,
    NavBar,
    FooterComponent,
    VAccordeon
  },

  data() {
    return {
      isNavbarFixed: false
    };
  },

  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },

  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },

  methods: {
    handleScroll() {
      this.isNavbarFixed = window.scrollY !== 0;
    }
  }
};
</script>

<style>
main-page {
  background-color: white;
  margin-bottom: 5vh;
}

.line {
  width: 100%;
}
</style>
