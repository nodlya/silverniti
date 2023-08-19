<template>
  <div class="wrapper">
    <h1>ПАРТНЁРЫ</h1>
    <div>
      <div
        v-for="{ locality, body } in partners_info"
        :key="locality + body"
        class="section"
      >
        <h2>{{ locality }}</h2>

        <swiper
          :slides-per-view="1"
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
  </div>
</template>

<script>
import PartnerCard from "./PartnerCard.vue";

import partners_info from "../partners_info";

import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation } from "swiper/modules";
import "swiper/css";
import "swiper/css/navigation";

export default {
  name: "PartnersContent",
  components: {
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
  }
};
</script>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  gap: 40px;
}

swiper-slide {
  width: fit-content;
  display: flex;
  flex-direction: row;
  justify-content: center;
}

h1 {
  margin-left: 40px;
  margin-bottom: 24px;
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
  .swiper-button-next,
  .swiper-button-prev {
    --swiper-navigation-size: 20px;
    margin: 0 -8px 0 -8px;
  }
}
</style>
