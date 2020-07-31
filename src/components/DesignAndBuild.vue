<template>
    <div class="wrap">
            <section class="design-wrapper">
                <div class="design-content">
                    <h2 class="section-title">
                        Design & Build Your Own Landing Pages
                    </h2>
                    <p class="section-description">
                        Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus
                        mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.
                    </p>
                    <div class="first-block-cards">
                           <w-card />                     
                    </div>
                </div>
                <div class="first-block-about-device">
                    <img src="/img/phone-device.jpg" alt="phone">
                </div>
        </section>
        </div>
</template>

<script>
import WCard from "@/widgets/WCard"

export default {
    name: 'DesignAndBuild',
    components: {
        WCard
    }
}
</script>

<style lang="scss" scoped>
.design-wrapper {
    padding-top: 100px;
    display: flex;
    justify-content: space-between;
}
.design-content {
    max-width: 520px;
}
</style>