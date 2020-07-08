<template>
    <div class="wrap">
        <section class="second-section">
            <div class="second-section-wrapper">
                <section-title class="second-section-title">Light, Fast & Powerful</section-title>
                <section-desc class="second-section-desc"></section-desc>                           
            </div>
        </section> 
    </div>
</template>

<script>
import SectionTitle from '../widgets/section-title/Title'
import SectionDesc from '../widgets/section-desc/Desc'

export default {
    name: 'second-section',
    components: {
        SectionTitle,
        SectionDesc,       
    }
}
</script>

<style lang="scss" scoped>
.second-section {
    padding: 160px 0;
    background: #fff url('../assets/img/second-block-bg.svg') no-repeat left center;
    display: flex;
    justify-content: flex-end;
}
.second-section-wrapper {
    max-width: 445px;
}
.second-section-title {
    margin-bottom: 16px;
}
</style>
