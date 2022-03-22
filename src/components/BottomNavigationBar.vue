<template>
  <div class="bottom-nav">
  <a href="#"><ion-icon name="home"></ion-icon></a>
  <a href="#"><ion-icon name="search"></ion-icon></a>
  <a href="#"><ion-icon name="chatbubbles"></ion-icon></a>
  <a href="#"><ion-icon name="contact"></ion-icon></a>
  </div>
</template>

<script>
export default {
  name: "BottomNavigationBar",
}
</script>

<style scoped>
 .bottom-nav {
   position: fixed;
   display: flex;
   bottom: 0;
   width: 100%;
   justify-content: space-between;
 }

 .bottom-nav a {
   text-decoration: none;
   display: inline-block;
   width: calc(100% / 4);
   text-align: center;
   border-top: transparent 4px solid;
 }

 .bottom-nav a:active {
   border-top: #99319B 4px solid;
 }

 ion-icon {
   font-size: 50px;
   padding: 10px;
 }
</style>