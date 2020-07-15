<template>
  <main class="main">
    <div class="header-intro-bg"></div>
    <intro />
    <first-section />
    <second-section />
    <third-section />
    <fourth-section />
    <price-section />
  </main>
</template>

<script>
import Intro from '@/components/Intro'
import FirstSection from '@/components/FirstSection'
import SecondSection from '@/components/SecondSection'
import ThirdSection from '@/components/ThirdSection'
import FourthSection from '@/components/FourthSection'
import PriceSection from '@/components/PriceSection'

export default {
  name: 'Home',
  components: {
    Intro,
    FirstSection,
    SecondSection,
    ThirdSection,
    FourthSection,
    PriceSection
  }
}
</script>

<style lang="scss" scoped>
.header-intro-bg {
    position: absolute;
    margin: 0 auto;
    display: flex;
    width: 100%;
    max-width: 1440px;
    min-height: 1110px;
    background: #fff url('/img/intro-bg.svg') no-repeat right top;
    background-size: 71%;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    z-index: -1;
}
</style>
