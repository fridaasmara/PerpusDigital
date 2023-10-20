<template>
  <div>
    <div class="navbar">
      <div class="brand">
        <img src="" alt="" />
        <p>Perpus Digital</p>
      </div>
      <div class="menu">
        <a href="">Home</a>
        <a href="">About</a>
        <a href="">Kunjungan</a>
        <a href="">Riwayat</a>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
* {
  margin: 0;
  padding: 0;
}

.navbar {
  background-color: blue;
  color: white;
  display: flex;
  justify-content: space-around;
}

.brand p {
  font-size: 30px;
}

.menu {
  float: right;
  background-color: black;
  padding-right: 10px;
}

a {
  padding-right: 50px;
  font-size: 20px;
  text-decoration: none;
  color: white;
}
</style>
