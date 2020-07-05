<template>
    <div class="wrap">
        <section class="first-section">
            <div class="first-section-wrapper">
                <section-title></section-title>
                <section-desc></section-desc>
            <!-- <div class="first-block-cards">
                <div class="first-block-card">
                    <img class="card-icon" src="./img/first-block-icon.png" alt="icon">
                    <h3 class="card-title">
                        Title Goes Here
                    </h3>
                    <p class="card-desc">
                        Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. 
                    </p>
                </div>
                <div class="first-block-card">
                    <img class="card-icon" src="./img/first-block-icon.png" alt="icon">
                    <h3 class="card-title">
                        Title Goes Here
                    </h3>
                    <p class="card-desc">
                        Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. 
                    </p>
                </div> 
            </div> -->
            </div>
        </section> 
    </div>
</template>

<script>
import SectionTitle from '../widgets/section-title/Title'
import SectionDesc from '../widgets/section-desc/Desc'
export default {
    name: 'first-section',
    components: {
        SectionTitle,
        SectionDesc
    }
}
</script>

<style lang="scss" scoped>

</style>
