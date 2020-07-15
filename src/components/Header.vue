<template>
  <div class="wrap">
    <header class="header">
      <navigation />
      <router-link to="/" class="logo">Landie</router-link>
      <w-button type="button" size="md" color="dark">Buy Now</w-button>
    </header>
  </div>
</template>

<script>
import WButton from '@/widgets/WButton'
import Navigation from '../components/Nav'

export default {
  name: 'header-app',
  components: {
    WButton,
    Navigation
  }
}
</script>
<style lang="scss">
.header {
  width: 100%;
  display: flex;
  justify-content: space-between;
  padding: 16px 0;
  align-items: center;
  z-index: 3;
}

.logo {
  font-weight: 900;
  font-size: 2.6em;
  color: #37447E;
  transition: 0.2s;
  cursor: pointer;

  &:hover {
    color: rgb(255, 0, 212);
  }
}
</style>
