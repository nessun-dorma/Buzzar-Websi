<template>
  <NavigationBar :window-size=this.windowsSize />
</template>

<script>
import NavigationBar from "@/components/NavigationBar";
export default {
  name: 'App',
  data: function (){
    return {
      windowsSize: 0,
    }
  },
  components: {
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
