<template>
    <div class="section-card">
        <img class="card-icon" :src="src" :alt="alt">
        <h3 class="card-title">
            <slot name="title">Title Goes Here</slot>
        </h3>
        <p class="card-description">
            <slot name="description">
                Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. 
            </slot>
        </p>
    </div>
</template>

<script>
export default {
    name: 'WCard',
    props: {
        src: {
            type: String,
            required: true
        },
        alt: {
            type: String,
            required: true
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
.card-description {
    font-size: 12px;
    line-height: 18px;
    color: #5D6970;
}
</style>