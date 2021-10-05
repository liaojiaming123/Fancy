<template>
  <div class="home">
    <Fancy />
  </div>
</template>

<script>
import Fancy from '@/components/Fancy.vue'
// import Navbar from '@/components/Navbar.vue'

export default {
  name: 'Home',
  components: {
    Fancy
  }
}
</script>
<style>
.home{
  margin: 0 0.25em;
}
</style>
