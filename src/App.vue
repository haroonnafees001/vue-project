<template>
  <div id="app">
    <Header/>
    <Dashboard/>
  </div>
</template>

<script>
import Dashboard from './components/DashBoard.vue'
import Header from './components/TheHeader.vue'

export default {
  name: 'App',
  components: {
    Dashboard,
    Header
  }
}
</script>

