<template>
  <div>
    <nav-bar />
    <div class="content">
      <main-page />

      <img
        src="./assets/divider.png"
        class="divider"
      />

      <h1>ПАРТНЁРЫ</h1>
      <div  class="sections">
        <div
          v-for="{ locality, body } in partners_info"
          :key="locality+body"
          class="section"
        >
          <h2>{{ locality }}</h2>

          <swiper
            :slides-per-view="1"
            :space-between="50"
            :navigation="true"
            :modules="modules"
            :centered-slides="true"
            @swiper="onSwiper"
            @slide-change="onSlideChange"
          >
            <swiper-slide
              v-for="(partner, index) in body"
              :key="index"
            >
              <div class="slide-content">
                <partner-card
                  :partner-logo-name="partner.partnerLogoName"
                  :partner-name="partner.partnerName"
                  :partner-link-list="partner.partnerLinksList"
                />
              </div>
            </swiper-slide>
          </swiper>
        </div>
      </div>
      <footer-component />
    </div>
    <!-- <v-accordeon title="Вконтакте"></v-accordeon> -->
  </div>
</template>

<script>
import MainPage from "./components/MainPage.vue";
import NavBar from "./components/NavBar.vue";
import FooterComponent from "./components/FooterComponent.vue";
import PartnerCard from "./components/PartnerCard.vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css/navigation";
import { Navigation } from "swiper/modules";
import "swiper/css";
import VAccordeon from "./components/VAccordeon.vue";

export default {
  name: "App",
  components: {
    MainPage,
    NavBar,
    FooterComponent,
    PartnerCard,
    Swiper,
    SwiperSlide
  },

  setup() {
    return {
      modules: [Navigation]
    };
  },

  data() {
    return {
      partners_info
    };
    VAccordeon
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

swiper-slide {
  width: fit-content;
  display: flex;
  flex-direction: row;
  justify-content: center;
}

nav-bar {
  z-index: 10000;
}

.content {
  padding-top: 130px;
  color: black;
}

.divider {
  margin: 80px 0 80px 0;
  width: 100%;
  height: auto;
}

h1 {
  margin-left: 40px;
  margin-bottom: 24px;
}

.sections {
  margin: 0 40px 0 40px;
}

.section {
  margin: 16px 0 8px 0;
}

.slide-content {
  width: 90%;
  margin-left: 5%;
  padding: 8px;
  display: flex;
  flex-direction: row;
  justify-content: center;
}

/* .slide-content {
  padding: 0 16px 0 16px;
  display: inline-block;
  width: auto;
  margin: 0 40px; /* Задайте отступы между карточками 
} */

.cards {
  display: flex;
  flex-direction: row;
  gap: 16px;
  margin: 16px;
}

.swiper-button-next {
  --swiper-navigation-color: black;
}

.swiper-button-prev {
  --swiper-navigation-color: black;
}

@media (max-width: 900px) {
  .swiper-button-next, .swiper-button-prev{
    --swiper-navigation-size: 20px;
    margin: 0 -8px 0 -8px;
  }
}
</style>
