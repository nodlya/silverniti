<template>
  <div>
    <nav-bar />
    <div class="content">
      <main-page />
      <img
        src="./assets/Line 4.png"
        class="line"
      />
      <div class="sections">
        <div
          v-for="{ locality, body } in partners_info"
          :key="locality"
          class="section"
        >
          <h2>{{ locality }}</h2>
          <div
            v-for="{ id, partnerLogoName, partnerName, partnerLinksList } in body"
            :key="id"
            class="cards"
          >
            <partner-card
              :partner-logo-name="partnerLogoName"
              :partner-name="partnerName"
              :partner-link-list="partnerLinksList"
            />
          </div>
        </div>
      </div>
      <footer-component />
    </div>
    <v-accordeon title="Вконтакте"></v-accordeon>
  </div>
</template>

<script>
import MainPage from "./components/MainPage.vue";
import NavBar from "./components/NavBar.vue";
import FooterComponent from "./components/FooterComponent.vue";
import PartnerCard from "./components/PartnerCard.vue";
import partners_info from "./partners_info.js";

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
      partners_info
    };
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
  color: black;
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
