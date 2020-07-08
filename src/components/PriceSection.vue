<template>
    <section class="price-section">
        <section-title>
            A Price To Suit Everyone
        </section-title>
        <section-desc></section-desc>    
        
        <span class="price-section-cost">
            $40
        </span>
        <span class="price-block-desc-for-cost">
            UI Design Kit
        </span>
        <span class="price-block-note">
            See, One price. Simple.
        </span>
        <button class="price-block-btn darker-btn">
            Purchase Now
        </button>
    </section>
</template>

<script>
import SectionTitle from '../widgets/section-title/Title'
import SectionDesc from '../widgets/section-desc/Desc'
import Wbutton from '../widgets/button/Wbutton'

export default {
    name: 'price-block',
    components: {
        SectionTitle,
        SectionDesc,
        Wbutton
    }
}
</script>

<style lang="scss" scoped>

</style>