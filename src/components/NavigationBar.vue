<template>
  <nav class="main-nav">
<div class="logo-div">
  <img alt="Buzzar logo" src="../assets/Logo.svg" class="logo">
</div>
  <div class="nav-div">
    <ul class="nav-list">
      <li v-if="windowSize > 851"><a href="#">Contact</a></li>
      <li v-if="windowSize > 851"><a href="#">FAQ</a></li>
      <li v-if="windowSize > 851"><a href="#">Help</a></li>
      <li><a href="#">Become a Seller</a></li>
    </ul>
  </div>
  </nav>
<!--  <div>{{ this.windowSize }}</div>-->
</template>

<script>
export default {
  name: "NavigationBar",
  props: ["windowSize"]
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');

  .main-nav {
    display: flex;
    justify-content: space-between;
    width: 100vw;
  }

  .logo-div, .nav-list, li, li a {
    display: inline-block;
    text-decoration: none;
  }

  .logo {
    padding: 2rem;
  }

  .nav-list li {
    list-style: none;
    margin: 35px 0 0 30px;
    padding: 15px 20px;
    font-family: 'Montserrat', sans-serif;
    font-weight: 600;
    color: #99319B;
  }

  .nav-list li:last-child{
    background: #99319B;
    margin-right: 25px;
    border-radius: 10px;
  }

  .nav-list li:last-child a {
    color: white;
  }
</style>