<template>
  <div id="app">
    <header-app></header-app>
    <router-view></router-view> 
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
@import url('./assets/css/reset.css');
@import url('./assets/css/fonts.css');

html {
    font-family: 'Roboto';
    font-size: 10px;
}
.wrap {
    max-width: 1150px;
    margin: 0 auto;
    padding: 0 20px;
}
</style>
