<template>
  <div class="background">
    <div class="card">
      <img
        alt="Image"
        :src="imageLink"
      />
      <div class="right-section">
        <p>{{ partnerName }}</p>
        <div class="links">
          <partner-link
            v-for="{ id, type, url } in partnerLinkList"
            :key="id"
            :type="type"
            :url="url"
          />
        </div>
      </div>
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

.background{
    width: 80%;
    display: flex;
    background-color: #f7f7f7;
    justify-content: center;
}
.card {
  display: flex;
  padding: 8px;
  color: black;
  height: 80px;
}

.right-section {
  margin-left: 24px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-end;
  padding: 4px;
  color: black;
}

.links {
  display: flex;
  flex-direction: row;
  gap: 8px;
}

img {
  width: auto;
  height: 64px;
}

@media (max-width: 900px) {
  img {
    max-width: 40%;
    height: auto;
    object-fit: contain;
  }

  .right-section {
    margin-left: 4px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: flex-end;
    padding: 4px;
    color: black;
    font-size: 10px;
  }
}

.bottom-section {
  padding: 10px;
}
</style>
