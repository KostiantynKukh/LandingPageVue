<template>
  <div id="app">
    <header-main />
    <router-view></router-view> 
  </div>
</template>

<script>
import HeaderMain from '@/components/Header'
export default {
  name: 'app',
  components: {
    HeaderMain
  }
}
</script>
<style lang="scss">
@import url('./assets/css/style.css');
</style>
