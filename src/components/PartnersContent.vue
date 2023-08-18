<template>
  <div
    v-for="{ locality, body } in partners_info"
    :key="locality"
  >
    <h2>{{ locality }}</h2>
    <div
      v-for="({ partnerLogoName, partnerName, partnerLinksList }, index) in body"
      :key="index"
      class="cards"
    >
      <partner-card
        :partner-logo-name="partnerLogoName"
        :partner-name="partnerName"
        :partner-link-list="partnerLinksList"
      />
    </div>
  </div>
</template>

<script>
import PartnerCard from "./PartnerCard.vue";

import partners_info from "../partners_info.js";

export default {
  name: "PartnersContent",
  components: {
    PartnerCard
  },

  data() {
    return {
      partners_info
    };
  }
};
</script>

<style scoped>
.cards {
  display: flex;
  flex-direction: row;
  gap: 16px;
  margin: 16px;
}
</style>
