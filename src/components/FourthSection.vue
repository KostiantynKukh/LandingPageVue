<template>
    <div class="wrap">
        <section class="fourth-section">
            <div class="fourth-section-wrapper">
                <h2 class="section-title fourth-section-title">Light, Fast & Powerful</h2>
                <p class="section-description fourth-section-description">
                    Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus 
                    mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.
                </p> 
                <w-button type="button" size="md" color="dark">Purchase Now</w-button>                           
            </div>
        </section> 
    </div>
</template>

<script>

import WButton from '@/widgets/WButton'

export default {
    name: 'FourthSection',
    components: {       
        WButton       
    }
}
</script>

<style lang="scss" scoped>
.fourth-section {
    padding: 160px 0;
    background: #fff url('/img/fourth-block-bg.svg') no-repeat left center;
    display: flex;
    justify-content: flex-end;
}
.fourth-section-wrapper {
    max-width: 445px;
}
.fourth-section-title {
    margin-bottom: 16px;
}
.fourth-section-description {
    margin-bottom: 40px;
}
</style>
