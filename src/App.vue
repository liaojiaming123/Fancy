<template>
    <Navbar />
    <Bg />
    <router-view />
</template>

<script>
import Bg from "@/components/Background.vue";
import Navbar from "@/components/Navbar.vue";

export default {
  name:'app',
  components:{
    Bg,Navbar
  }
}
</script>

<style>
body,html{
  overflow-x: hidden;
}
* {
  padding: 0;
  margin: 0;
}
#app {
  width: 100%;
  height: 100vh;
  overflow-x: hidden;
}
</style>
