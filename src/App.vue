<template>
  <div id="app">
    <header-app />
    <router-view />
  </div>
</template>

<script>
import HeaderApp from './components/Header'
export default {
  name: 'app',
  components: {
    HeaderApp
  }
}
</script>
<style lang="scss">
@import url('./assets/css/main.css');
</style>
