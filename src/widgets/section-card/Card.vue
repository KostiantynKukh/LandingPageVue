<template>
  <div class="section-card">
    <img class="card-icon" :src="content.imgSrc" alt="icon">
    <h3 class="card-title">
      {{ content.title }}
    </h3>
    <p class="card-desc">
      {{ content.text }}
    </p>
  </div>
</template>

<script>
const DEFAULT_CONTENT = {
  title: 'Title Goes Here',
  text: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor.',
  imgSrc: '/img/first-block-icon.png'
}

export default {
  name: 'section-card',
  props: {
    content: {
      type: Object,
      default: () => DEFAULT_CONTENT
    }
  }
}
</script>

<style lang="scss" scoped>
.section-card {
  cursor: pointer;
  transition: 0.3s;

  &:hover {
    transform: scale(0.95);
  }
}

.card-icon {
  max-width: 36px;
  margin-bottom: 14px;
}

.card-title {
  font-weight: 500;
  font-size: 1.6em;
  line-height: 26px;
  color: #091133;
  margin-bottom: 6px;
}

.card-desc {
  font-size: 12px;
  line-height: 18px;
  color: #5D6970;
}
</style>
