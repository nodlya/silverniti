<template>
  <div class="main-page">
    <img
      class="main-page__logo"
      src="../assets/logo.svg"
    />
    <p class="main-page__text">
      Первый в России Региональный конкурс и форум корпоративных изданий и сайтов, первая выставка
      корпоративных газет и журналов, прошедшие в Перми в 2005 году. Спустя три года – и тоже
      впервые в России – новый шаг в развитии проекта – Национальный конкурс корпоративных медиа.
    </p>
    <img
      class="main-page__timeline"
      alt="timeline"
      :src="timelineName"
    />
    <!-- TODO добавить ссылку куда должна вести кнопка -->
    <button class="main-page__button">ПОДРОБНЕЕ О ПРОЕКТЕ</button>
  </div>
</template>

<script>
export default {
  name: "MainPage",
  data() {
    return {
      width: 0
    };
  },

  computed: {
    timelineName() {
      return this.width > 900 ? "src/assets/timeline.png" : "src/assets/timeline-mobile.svg";
    }
  },

  created() {
    window.addEventListener("resize", () => (this.width = window.innerWidth));
  }
};
</script>

<style scoped>
.main-page {
  width: 100%;
  display: grid;
  grid-template: 412px 100px auto / 50% 50%;
  grid-template-areas:
    "logo text"
    "timeline timeline"
    ". button";
  align-items: center;
  justify-content: center;
  row-gap: 50px;
  padding: 0 50px;

  .main-page__logo {
    grid-area: logo;
    padding-right: 75px;
    width: 100%;
    align-self: flex-start;
  }

  .main-page__text {
    grid-area: text;
    width: 100%;
    font-size: 23px;
    text-align: right;
    padding-left: 75px;
  }

  .main-page__timeline {
    width: 100%;
    grid-area: timeline;
  }

  .main-page__button {
    grid-area: button;
    font-size: 20px;
    font-weight: 600;
    padding: 0.7em 2.1em;
    color: aliceblue;
    background-color: black;
    width: 50%;
    justify-self: right;
  }
}

@media (max-width: 900px) {
  .main-page {
    display: flex;
    flex-direction: column;

    .main-page__logo {
      padding-bottom: 25px;
      padding-right: 0;
    }

    .main-page__text {
      padding-left: 0;
    }

    .main-page__button {
      font-size: 16px;
    }
  }
}
</style>
