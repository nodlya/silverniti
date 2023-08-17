<template>
  <div class="container">
    <div class="main-page-grid">
      <div class="box-1">
        <img
          class="main-page_img1"
          src="../assets/1.svg"
        />
      </div>
      <div class="box-2">
        <p class="main-page_text">
          Первый в России Региональный конкурс и форум корпоративных изданий и сайтов, первая
          выставка корпоративных газет и журналов, прошедшие в Перми в 2005 году. Спустя три года –
          и тоже впервые в России – новый шаг в развитии проекта – Национальный конкурс
          корпоративных медиа.
        </p>
      </div>
    </div>
    <div class="box-3">
      <img
        class="main-page_img2"
        src="../assets/timeline.png"
      />
    </div>
    <button class="buttonclick">ПОДРОБНЕЕ О ПРОЕКТЕ</button>
  </div>
</template>

<script>
export default {
  name: "MainPage"
};
</script>

<style scoped>
.container {
    background-color: white;
    color: black;
    justify-content: center;
    margin-bottom: 25vh;
}

.main-page-grid {
  width: 100%;
  display: grid;
  grid-template-columns: 50% 50%;
}

[class^="box-"] {
  display: grid;
  place-items: center;
}

.main-page_img1 {
    height: auto;
    width: 80%;
}

.main-page_img2 {
    height: auto;
    width: 90%;
}

.main-page_text {
    width: 70%;
    font-size: 23px;
    text-align: right;
    text-transform: uppercase;
    margin-top: 90px;
}

.box-3 {
    margin-top: 10%;
    margin-bottom: 5%;
    height: auto;
}

button {
  font-size: 20px;
  float: right;
  margin-right: 45px;
  padding: 0.7em 2.1em;
  color: aliceblue;
  background-color: black;
}
</style>
