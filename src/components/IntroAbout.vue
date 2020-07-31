<template>
    <div class="wrap">
            <section class="design-wrapper">
                <div class="design-content">
                    <h2 class="section-title design-title">
                        Design & Build Your Own Landing Pages
                    </h2>
                    <p class="section-description design-description">
                        Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus
                        mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.
                    </p>                    
                    <div class="design-block-cards">
                        <w-card src="/img/first-block-icon.png" alt="card_icon" class="design-section-card"></w-card>
                        <w-card src="/img/first-block-icon.png" alt="card_icon" class="design-section-card"></w-card>
                        <w-card src="/img/first-block-icon.png" alt="card_icon" class="design-section-card"></w-card>
                        <w-card src="/img/first-block-icon.png" alt="card_icon" class="design-section-card"></w-card> 
                    </div>                                           
                    
                </div>                
                <img src="/img/phone-device.jpg" alt="phone">                
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
.design-title {
    margin-bottom: 16px;
}
.design-description {
    margin-bottom: 70px;
}
.design-block-cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}
.design-section-card {
    max-width: 245px;
    display: inline-block;
    margin-bottom: 30px;
}

</style>