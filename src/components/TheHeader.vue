<template>
  <div>
    <Navbar  @isMenuOpened="isMenuOpened"/>
    <Sidebar :menuOpen="isMenuActive"/>
  </div>

</template>


<script>

import Sidebar from './header/TheSidebar.vue'
import Navbar from './header/TheNavbar.vue'

export default {
  name: "TheHeader",
  components: {
    Sidebar,
    Navbar
  },
  data: function () {
    return {
      isMenuActive:false
    }
  },
  methods: {
    isMenuOpened (event) {
      this.isMenuActive = event;
    }
  }
}
</script>

<style scoped>

</style>