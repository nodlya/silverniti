<template>
    <div class="container">
        <div class="main-page-grid">
            <div class="box-1">
                <img class="main-page_img1" src="../assets/1.svg" />
            </div>
            <div class="box-2">
                <p class="main-page_text">
                    Первый в России Региональный конкурс и форум корпоративных изданий и сайтов, первая выставка
                    корпоративных газет и журналов, прошедшие в Перми в 2005 году. Спустя три года – и тоже впервые в России
                    – новый шаг в развитии проекта – Национальный конкурс корпоративных медиа.
                </p>
            </div>
        </div>
        <div class="box-3">
            <img class="main-page_img2" src="../assets/timeline.png" />
        </div>
        <button class="buttonclick">ПОДРОБНЕЕ О ПРОЕКТЕ</button>
    </div>
</template>

<script>
export default {
    name: "MainPage",
};
</script>

<style scoped>
.container {
    background-color: white;
    color: black;
    justify-content: center;
    margin-bottom: 40vh;
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
    height: 75%;
    width: auto;
}

.main-page_img2 {
    height: auto;
    width: auto;
}

.main-page_text {
    width: 84%;
    font-size: 23px;
    text-align: right;
    text-transform: uppercase;
    margin-top: 90px;
}

.box-3 {
    margin-top: 60px;
    margin-bottom: 60px;
}

button {
    font-size: 20px;
    float: right;
    margin-right: 45px;
    padding: .7em 2.1em;
    color: aliceblue;
    background-color: black;
}
</style>