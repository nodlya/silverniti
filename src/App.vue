<template>
  <div>
    <nav-bar />
    <div class="content">
      <main-page />
      <img src="./assets/Line 4.png" class="line" />
      <footer-component />
    </div>
  </div>
</template>

<script>
import MainPage from './components/MainPage.vue';
import NavBar from './components/NavBar.vue';
import FooterComponent from './components/FooterComponent.vue';

export default {
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

.content{
  padding-top: 130px;
}

.line {
  width: 100%;
}
</style>
