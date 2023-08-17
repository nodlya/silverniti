<template>
  <div>
    <nav-bar />
    <div class="content">
      <main-page />
      <img src="./assets/Line 4.png" class="line" />
      <div class="sections">
        <div v-for="locality in partners_info" :key="locality.locality" class="section">
          <h2>{{ locality.locality }}</h2>
          <div v-for="partner in locality.body" :key="partner.id" class="cards">
            <partner-card partner-logo-name="partner.partnerLogoName" parnter-name="partner.partnerName" partner-link-list="partner.partnerLinkList" />
          </div>
        </div>
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
import partners_info from './partners_info.json'

export default {
  name: "App",
  components: {
    MainPage,
    NavBar,
    FooterComponent,
    PartnerCard
  },

  data() {
    return {
      jsonData: partners_info
    }
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

.cards {
  display: flex;
  flex-direction: row;
  gap: 16px;
  margin: 16px;
}
</style>
