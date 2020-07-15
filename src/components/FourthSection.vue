<template>
    <div class="wrap">
        <section class="fourth-section">
            <div class="fourth-section-wrapper">
                <section-title class="fourth-section-title">Light, Fast & Powerful</section-title>
                <section-desc class="fourth-section-desc">
                    Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus
                    mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.
                </section-desc>
                <Wbutton type="button" size="md" color="dark">Purchase Now</Wbutton>
            </div>
        </section>
    </div>
</template>

<script>
import SectionTitle from '../widgets/section-title/Title'
import SectionDesc from '../widgets/section-desc/Desc'
import Wbutton from '@/widgets/WButton'

export default {
    name: 'fourth-section',
    components: {
        SectionTitle,
        SectionDesc,
        Wbutton
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
.fourth-section-desc {
    margin-bottom: 40px;
}
</style>
