<template>
  <div>
    <nav-bar />
    <div class="content">
      <main-page />
      <img src="./assets/Line 4.png" class="line" />
      <div class="cards">
        <partner-card partner-num="5.png" />
        <partner-card partner-num="6.jpg" />
        <partner-card partner-num="10.jpg" />
      </div>
      <footer-component />
    </div>
  </div>
</template>

<script>
import MainPage from './components/MainPage.vue';
import NavBar from './components/NavBar.vue';
import FooterComponent from './components/FooterComponent.vue';
import PartnerCard from './components/PartnerCard.vue';

export default {
  name: "App",
  components: {
    MainPage,
    NavBar,
    FooterComponent,
    PartnerCard
  }

};
</script>

<style>
main-page {
  background-color: white;
  margin-bottom: 5vh;

}

.content {
  padding-top: 130px;
}

.line {
  width: 100%;
}

.cards{
  display: flex;
  flex-direction: row;
  gap: 16px;
  margin: 16px;
}
</style>
