<template>
    <div class="wrap">
        <section class="first-section">
            <div class="first-section-wrapper">
                <section-title class="first-section-title">Light, Fast & Powerful</section-title>
                <section-desc class="first-section-desc"></section-desc>
                <section-card class="first-section-card"></section-card>
                <section-card class="first-section-card"></section-card>            
            </div>
        </section> 
    </div>
</template>

<script>
import SectionTitle from '../widgets/section-title/Title'
import SectionDesc from '../widgets/section-desc/Desc'
import SectionCard from '../widgets/section-card/Card'
export default {
    name: 'first-section',
    components: {
        SectionTitle,
        SectionDesc,
        SectionCard
    }
}
</script>

<style lang="scss" scoped>
.first-section {
    padding: 160px 0;
    background: #fff url('../assets/img/first-block-bg.svg') no-repeat center right; 
}
.first-section-wrapper {
    max-width: 540px;    
}
.first-section-title {
    margin-bottom: 16px;
}
.first-section-desc {
    margin-bottom: 80px;
}
.first-section-card {
    max-width: 255px;
    display: inline-block;
    margin-right: 20px;
    &:last-child {
        margin-right: 0;
    }
}

</style>
