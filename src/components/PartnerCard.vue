<template>
  <div class="card">
    <img
      alt="Image"
      :src="imageLink"
    />
    <div class="right-section">
      <p>{{ partnerName }}</p>
      <partner-link
        v-for="{ id, type, url } in partnerLinkList"
        :key="id"
        :type="type"
        :url="url"
      />
    </div>
  </div>
</template>

<script>
import PartnerLink from "./PartnerLink.vue";

export default {
  name: "PartnerCard",
  components: {
    PartnerLink
  },

  props: {
    partnerName: {
      type: String,
      default: ""
    },

    partnerLogoName: {
      type: String,
      default: "0"
    },

    partnerLinkList: {
      type: Array,
      default: () => []
    }
  },

  computed: {
    imageLink() {
      return `/src/assets/partners_logo/${this.partnerLogoName}`;
    }
  }
};
</script>

<style scoped>
.card {
  display: flex;
  background-color: #f7f7f7;
  padding: 8px;
  color: black;
}

.right-section {
  margin-left: 8px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-end;
  padding: 4px;
  color: black;
}

img {
  width: auto;
  height: 64px;
}

.bottom-section {
  padding: 10px;
}
</style>
