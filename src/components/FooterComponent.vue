<template>
  <div>
    <footer id="contacts">
      <div class="footer_item">
        <div class="box-1">
          <p>
            КОНТАКТЫ<br /><br /><br />
            <a
              class="lien"
              href="https://silverniti.ru"
              >https://silverniti.ru</a
            ><br />
            action-nm@yandex.ru
          </p>
        </div>
        <div class="box-2">
          <a>
            <img
              src="../assets/footer.png"
              class="footer_img"
            />
          </a>
        </div>
      </div>
      <p class="footer_info">Разработано Институтом Информационных технологий ЧелГУ</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: "FooterComponent"
};
</script>

<style scoped>
footer p {
  color: white;
  font-size: 20px;
}

footer p a {
  color: white;
  text-decoration: none;
}

footer {
  width: 100%;
  height: auto;
  background-color: black;
}

.box-1 {
    padding: 30px 0px 30px 50px;
}

.box-2 {
    padding: 30px;
}

.footer_info {
  font-size: 16px;
  padding: 2vh 0 3vh 0;
}

@media (max-width: 480px) {
    footer p {
        font-size: 14px;
    }

    .footer_info {
        font-size: 10px;
    }

    .box-1 {
        padding: 10px 0px 10px 30px;
    }

    .box-2 {
        padding: 10px;
    }


    .footer_img {
        width: 90%;
        height: auto;
        float: right;
        margin-right: 0px !important;
    }
}

.footer_item {
  display: flex;
  justify-content: space-between;
}

.footer_img {
    width: 90%;
    height: auto;
    float: right;
    margin-right: 60px;
}

.footer_info {
  text-align: center;
}
</style>
