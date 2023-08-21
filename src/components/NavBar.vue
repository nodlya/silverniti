<template>
  <ul class="navbar-menu">
    <li>
      <a href="#partners"> РЕГИОНЫ </a>
    </li>
    <li>
      <a href="#links">МЕДИАРЕСУРСЫ</a>
    </li>
    <li>
      <a href="#footer">КОНТАКТЫ</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: "NavBar"
};
</script>

<style scoped>
.navbar-menu {
  height: 60px;
  list-style-type: none;
  padding-left: 0;
  padding-right: 3.5%;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: white;
  margin: 0;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  z-index: 2;
  /* box-shadow: 0px 1px 5px rgba(0, 0, 0, 0.1); */
}

.navbar-menu li {
  margin-right: 20px;
}

.navbar-menu li:last-child {
  margin-right: 0;
}

.navbar-menu li a {
  font-size: 20px;
  text-decoration: none;
  color: #000;
  padding: 10px;
}

@media (max-width: 900px) {
  .navbar-menu li a {
    font-size: 14px;
  }

  .navbar-menu li {
    margin-right: 5px;
  }
}
</style>
