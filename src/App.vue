<template>
  <NavigationBar :window-size=this.windowsSize />
  <BottomNavigationBar v-if="windowsSize < 850"/>
</template>

<script>
import NavigationBar from "@/components/NavigationBar";
import BottomNavigationBar from "@/components/BottomNavigationBar";
export default {
  name: 'App',
  data: function (){
    return {
      windowsSize: window.innerWidth,
    }
  },
  components: {
    BottomNavigationBar,
    NavigationBar
  },
  watch: {
    windowsSize(){
      console.log(this.windowsSize)
    }
  },
  mounted() {
    window.addEventListener("resize", () => {
        this.windowsSize = window.innerWidth
    })
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
