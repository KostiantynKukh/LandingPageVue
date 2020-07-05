<template>
  <main class="main">
    <div class="header-intro-bg"></div>
    <intro></intro>
    <first-section></first-section>
  </main>
</template>

<script>
import Intro from '../components/Intro'
import FirstSection from '../components/FirstSection'
export default {
  name: 'Home',
  components: {
    Intro,
    FirstSection
  }
}
</script>

<style lang="scss" scoped>
.header-intro-bg {
    position: absolute;
    display: block;
    width: 100%;
    min-height: 1110px;
    background: #fff url('../assets/img/intro-bg.svg') no-repeat right top;
    background-size: 71%;
    top: 0;
    left: 0;
    z-index: -1;
}
</style>
