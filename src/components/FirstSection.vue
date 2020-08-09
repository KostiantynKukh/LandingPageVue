<template>
    <div class="wrap">

        <section class="first-section">
            <div class="first-section-wrapper">
                <h2 class="section-title first-section-title">Light, Fast & Powerful</h2>
                <p class="section-description first-section-description">
                    Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus 
                    mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.
                </p>
                <w-card src="/img/first-block-icon.png" alt="card_icon" class="first-section-card"></w-card>
                <w-card src="/img/first-block-icon.png" alt="card_icon" class="first-section-card"></w-card>
            </div>
        </section> 

    </div>
</template>

<script>
import WCard from '@/widgets/WCard'

export default {
    name: 'FirstSection',
    components: {       
        WCard
    }
}
</script>

<style lang="scss" scoped>
.first-section {
    padding: 160px 0;
    background: #fff url('/img/first-block-bg.svg') no-repeat center right; 
}
.first-section-wrapper {
    max-width: 540px;    
}
.first-section-title {
    margin-bottom: 16px;
}
.first-section-description {
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
