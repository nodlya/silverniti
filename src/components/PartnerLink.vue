<template>
  <div>
    <a
      :href="url"
      :class="{ header: header }"
    >
      <span>{{ type }}</span>
      <img src="../assets/link.png" />
    </a>
  </div>
</template>

<script>
export default {
  name: "PartnerLink",
  props: {
    type: {
      type: String,
      default: ""
    },

    url: {
      type: String,
      default: ""
    },

    header: {
      type: Boolean
    }
  }
};
</script>

<style scoped>
div {
  color: black;
}
a {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 5px;
  font-size: 12px;
  text-transform: uppercase;
  text-decoration: none;
  color: black;
}
span {
  font-size: 18px;
}

a :hover {
  text-decoration: underline;
}

.header {
  font-size: 22px;
  text-transform: capitalize;
}

img {
  height: 16px;
  width: auto;
}

@media (max-width: 900px) {
  a {
    font-size: 10px;
  }

  span {
    font-size: 10px;
  }

  img {
    height: 8px;
  }
}
</style>
