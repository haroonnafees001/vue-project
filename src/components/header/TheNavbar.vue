<template>
  <div class="navbar">
    <span class="material-symbols-outlined ml-10 icon" @click="menuOpen">menu</span>
    <ul class="navbar-wrap">
        <li>
          <span class="material-symbols-outlined">notifications</span>
        </li>
        <li>
          <a class="dropdown-toggle">
            <img src="../../assets/profile.jpeg" alt="">
            <span class="mr-5">Administrator</span>
            <span class="material-symbols-outlined icon">expand_more</span>
          </a>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "TheNavbar",

  data: function () {
    return {
      isMenuOpened:false
    }
  },
  mounted() {
  },
  methods: {
    menuOpen () {
      this.isMenuOpened = !this.isMenuOpened;
      this.$emit('isMenuOpened',this.isMenuOpened)
    }
  }
}
</script>

<style scoped>

</style>