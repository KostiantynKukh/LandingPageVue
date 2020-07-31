<template>
    <section class="price-section">
        <div class="price-section-wrap">

            <h2 class="section-title price-section-title">Light, Fast & Powerful</h2>
            <p class="section-description price-section-description">
                Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus 
                mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.
            </p>       
            <span class="price-section-cost">
                $40
            </span>
            <span class="price-section-desc-for-cost">
                UI Design Kit
            </span>
            <span class="price-section-note">
                See, One price. Simple.
            </span>
            <w-button size="lg" color="dark" type="button">
                Purchase Now
            </w-button>

        </div>
    </section>
</template>

<script>

import WButton from '@/widgets/WButton'

export default {
    name: 'price-section',
    components: {        
        WButton
    }
}
</script>

<style lang="scss" scoped>
.price-section {
    padding: 230px 0 170px;    
    max-width: 1440px;
    margin: 0 auto;
    background: #fff url('/img/price-block-bg.svg') no-repeat center top;
}
.price-section-wrap {
    margin: 0 auto;
    max-width: 600px;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.price-section-title {
    margin-bottom: 16px;
}
.price-section-description {
    margin-bottom: 35px;
    text-align: center;

}
.price-section-cost {
    font-weight: 500;
    font-size: 5em;
    line-height: 66px;
    color: #222F65;
    text-align: center;
    letter-spacing: 1px;
}
.price-section-desc-for-cost {
    font-size: 1.6em;
    line-height: 26px;
    color: #37447E;
    margin-bottom: 60px;
}
.price-section-note {
    font-size: 1.4em;
    line-height: 24px;
    color: #5D6970;
    margin-bottom: 9px;
}
</style>