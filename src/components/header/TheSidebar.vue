<template>
  <div class="sidebar" :class="{'active':menuOpen}">
    <span class="material-symbols-outlined close-icon"  @click="menuOpen=!menuOpen">close</span>
    <div class="logo"><b>CRM.io</b></div>
    <ul class="menu">
      <li><a href="" class="active"><span class="material-symbols-outlined">dashboard</span>Dasboard</a></li>
      <li>
        <span class="submenu">Managment</span>
        <ul>
          <li><a href=""><span class="material-symbols-outlined">folder_open</span>Document</a></li>
          <li><a href=""><span class="material-symbols-outlined">contact_support</span>Contact</a></li>
          <li><a href=""><span class="material-symbols-outlined">psychology</span>Prospect</a></li>
          <li><a href=""><span class="material-symbols-outlined">rebase</span>Workflow</a></li>
        </ul>
      </li>

      <li>
        <span class="submenu">Connection</span>
        <ul>
          <li><a href=""><span class="material-symbols-outlined">headset_mic</span>Chat Integration</a></li>
          <li><a href=""><span class="material-symbols-outlined">linked_services</span>Marketing Automation</a></li>
          <li><a href=""><span class="material-symbols-outlined">email</span>Email Integration</a></li>
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