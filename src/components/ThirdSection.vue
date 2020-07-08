<template>
    <div class="wrap">
        <section class="third-section">
            <div class="third-section-wrapper">
                <section-title class="third-section-title">Light, Fast & Powerful</section-title>
                <section-desc class="third-section-desc"></section-desc>                           
            </div>
        </section> 
    </div>
</template>

<script>
import SectionTitle from '../widgets/section-title/Title'
import SectionDesc from '../widgets/section-desc/Desc'

export default {
    name: 'third-section',
    components: {
        SectionTitle,
        SectionDesc,       
    }
}
</script>

<style lang="scss" scoped>
.third-section {
    padding: 160px 0;
    background: #fff url('../assets/img/third-block-bg.svg') no-repeat left center;
    display: flex;
    justify-content: flex-end;
}
.third-section-wrapper {
    max-width: 445px;
}
.third-section-title {
    margin-bottom: 16px;
}
</style>
