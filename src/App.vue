<template>
  <div>
    <nav-bar />
    <main-page />
    <img src="./assets/Line 4.png" class="line" />
    <footer-component />
    <v-accordeon title="Вконтакте"></v-accordeon>
  </div>
</template>

<script>
import MainPage from './components/MainPage.vue';
import NavBar from './components/NavBar.vue';
import FooterComponent from './components/FooterComponent.vue';
import VAccordeon from "./components/VAccordeon.vue";

export default {
  data() {
    return {
      isNavbarFixed: false
    };
  },

  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },

  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },

  methods: {
    handleScroll() {
      this.isNavbarFixed = window.scrollY !== 0;
    }
  },
  
  name: "App",
  components: {
    MainPage,
    NavBar,
    FooterComponent
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
