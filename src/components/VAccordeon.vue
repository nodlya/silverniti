<!-- eslint-disable vue/attribute-hyphenation -->
<template>
  <div class="wrapper">
    <h1>МЕДИАРЕСУРСЫ ПАРТНЕРОВ</h1>
    <accordion
      class="container"
      multiple
    >
      <accordion-tab
        v-for="{ name, cards } in media"
        :key="name"
        :header="name"
        :pt="{
          root: { class: 'tab' },
          headerAction: { class: 'header' },
          headerTitle: { class: 'headerTitle' },
          content: { class: 'accordeon-content' }
        }"
        @click="open"
      >
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
            v-for="{ logoName, partner, url } in cards"
            :key="url"
          >
            <div class="slide-content">
              <partner-card
                :partnerName="partner"
                :partnerLogoName="logoName"
                :partner-link-list="url"
              />
            </div>
          </swiper-slide>
        </swiper>
      </accordion-tab>
    </accordion>
  </div>
</template>

<script>
import Accordion from "primevue/accordion";
import AccordionTab from "primevue/accordiontab";
import PartnerCard from "./PartnerCard.vue";

import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import { Navigation } from "swiper/modules";
import "swiper/css/navigation";

import { media } from "../media";

export default {
  name: "VAccordeon",
  components: {
    Accordion,
    AccordionTab,
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
      media,
      isOpened: false
    };
  },

  methods: {
    urlLink(url) {
      if (Array.isArray(url)) return url;
    },

    open() {
      this.isOpened = !this.opened;
    }
  }
};
</script>

<style>
.container {
  display: flex;
  flex-direction: column;
  width: 100%;
}
.header {
  display: flex !important;
  gap: 14px;
  padding: 0 14px;
}

.tab {
  padding: 30px 0;
  border-bottom: 1px solid #dcdcdc;
}

.headerTitle {
  font-size: 22px;
}

h1 {
  margin: 0 !important;
}

.wrapper {
  display: flex;
  flex-direction: column;
  gap: 40px;
}
.tab:focus {
  border: none;
}

.accordeon-content {
  padding-top: 30px;
}
swiper-slide {
  width: fit-content;
  display: flex;
  flex-direction: row;
  justify-content: center;
}
.slide-content {
  width: 90%;
  margin-left: 5%;
  padding: 8px;
  display: flex;
  flex-direction: row;
  justify-content: center;
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
