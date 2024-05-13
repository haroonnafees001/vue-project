<template>
  <div class="sidebar" :class="{'active':menuOpen}">
    <span class="material-symbols-outlined close-icon"  @click="menuOpen=!menuOpen">close</span>
    <div class="logo"><b>CRM.io</b></div>
    <ul class="menu">
      <li><a href="" class="active"><span class="material-symbols-outlined">dashboard</span>Documents</a></li>
      <li>
        <span class="submenu">Managment</span>
        <ul>
          <li><a href=""><span class="material-symbols-outlined">dashboard</span>Documents</a></li>
          <li><a href=""><span class="material-symbols-outlined">dashboard</span>Documents</a></li>
          <li><a href=""><span class="material-symbols-outlined">dashboard</span>Documents</a></li>
          <li><a href=""><span class="material-symbols-outlined">dashboard</span>Documents</a></li>
        </ul>
      </li>

      <li>
        <span class="submenu">Managment</span>
        <ul>
          <li><a href=""><span class="material-symbols-outlined">dashboard</span>Documents</a></li>
          <li><a href=""><span class="material-symbols-outlined">dashboard</span>Documents</a></li>
          <li><a href=""><span class="material-symbols-outlined">dashboard</span>Documents</a></li>
          <li><a href=""><span class="material-symbols-outlined">dashboard</span>Documents</a></li>
        </ul>
      </li>

    </ul>
  </div>


</template>

<script>
export default {
  name: "TheSidebar",
  props: ['menuOpen'],
  data: function () {
    return {
      isMenuClosed:''
    }
  },

}
</script>

<style scoped>

</style>