<template>
  <div @click="open">
    <div class="wrapper">
      <span class="title">{{ title }}</span>
      <div :class="{ open: isOpened }">
        <svg
          width="43"
          height="43"
          viewBox="0 0 43 43"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M6.16919 15.1664L21.0612 30.3687L35.9533 15.1664L33.4716 12.6312L21.0612 25.3018L8.6509 12.6312L6.16919 15.1664Z"
            fill="black"
          />
        </svg>
      </div>
    </div>

    <div v-if="isOpened">
      <slot />
    </div>
  </div>
</template>

<script>
export default {
  name: "VAccordeon",
  props: {
    title: {
      type: String,
      default: ""
    }
  },

  data() {
    return {
      isOpened: false
    };
  },

  methods: {
    open() {
      this.isOpened = !this.isOpened;
    }
  }
};
</script>

<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 28px 14px;
}
.title {
  font-size: 28px;
}
.open {
  transform: rotate(180deg);
}
</style>
