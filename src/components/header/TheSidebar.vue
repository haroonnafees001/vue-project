<template>
  <div class="sidebar" :class="{'active':menuOpen}">
    <span class="material-symbols-outlined close-icon"  @click="menuOpen=!menuOpen">close</span>
    <div class="logo"><b>CRM.io</b></div>
    <VuePerfectScrollbar class="scroll-area" v-once :settings="settings" @ps-scroll-y="scrollHandle">
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

        <li>
          <span class="submenu">Connection</span>
          <ul>
            <li><a href=""><span class="material-symbols-outlined">headset_mic</span>Chat Integration</a></li>
            <li><a href=""><span class="material-symbols-outlined">linked_services</span>Marketing Automation</a></li>
            <li><a href=""><span class="material-symbols-outlined">email</span>Email Integration</a></li>
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
    </VuePerfectScrollbar>
  </div>


</template>

<script>
import VuePerfectScrollbar from 'vue-perfect-scrollbar'

export default {
  name: "TheSidebar",
  props: ['menuOpen'],
  components: {
    VuePerfectScrollbar,
  },
  data: function () {
    return {
      isMenuClosed:'',
      settings: {
        maxScrollbarLength: 60
      }
    }
  },

}
</script>

<style scoped>

</style>