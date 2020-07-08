<template>
    <p class="section-desc">
        <slot />
    </p>
</template>

<script>
export default {
    name: 'section-desc'
}
</script>

<style lang="scss" scoped>
.section-desc {
    font-size: 1.6em;
    line-height: 26px;
    color: #6F7CB2;
}
</style>