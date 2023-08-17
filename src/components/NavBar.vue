<template>
  <nav class="navbar">
    <div class="container">
      <ul class="navbar-menu">
        <li><a href="#">РЕГИОНЫ</a></li>
        <li><a href="#">МЕДИАРЕСУРСЫ</a></li>
        <li><a href="#">КОНТАКТЫ</a></li>
      </ul>
    </div>
  </nav>
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
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: white;
  margin: 0;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  box-shadow: 0px 1px 5px rgba(0, 0, 0, 0.1);
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
</style>
