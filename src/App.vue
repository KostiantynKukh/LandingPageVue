<template>
  <div id="app">
    <header-component />
    <router-view></router-view>
    <footer-component />
  </div>
</template>

<script>
import HeaderComponent from '@/components/HeaderComponent'
import FooterComponent from '@/components/FooterComponent'

export default {
  name: 'app',
  components: {
    HeaderComponent,
    FooterComponent
  }
}
</script>
<style lang="scss">
@import url('./assets/css/style.css');
</style>
