<template>
    <h2 class="section-title">
        <slot />
    </h2>
</template>

<script>
export default {
    name: 'section-title'
}
</script>

<style lang="scss" scoped>
.section-title {
    font-weight: 500;
    color: #091133;
    font-size: 3.6em;
    line-height: 48px;    
}
</style>