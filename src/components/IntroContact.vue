<template>
    <div class="wrap">
            <section class="intro-contact-wrapper">
                <img src="/img/boy&girl.jpg" alt="phone">                

                <div class="intro-contact-content">
                    <h2 class="section-title intro-contact-title">
                        Light, Fast & Powerful
                    </h2>
                    <p class="section-description intro-contact-description">
                        Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus
                        mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.
                    </p>                    
                    <div class="intro-contact-block-cards">
                        <w-card src="/img/first-block-icon.png" alt="card_icon" class="intro-contact-section-card"></w-card>
                        <w-card src="/img/first-block-icon.png" alt="card_icon" class="intro-contact-section-card"></w-card>
                        <w-card src="/img/first-block-icon.png" alt="card_icon" class="intro-contact-section-card"></w-card>
                        <w-card src="/img/first-block-icon.png" alt="card_icon" class="intro-contact-section-card"></w-card> 
                    </div>                                           
                    
                </div>                
        </section>
        </div>
</template>

<script>
import WCard from '@/widgets/WCard'

export default {
    name: 'IntroContact',
    components: {
        WCard
    }
}
</script>

<style lang="scss" scoped>
.intro-contact-wrapper {
    display: flex;
    justify-content: space-between;
}
.intro-contact-content {
    max-width: 520px;
}
.intro-contact-title {
    margin-top: 100px;
    margin-bottom: 16px;
}
.intro-contact-description {
    margin-bottom: 70px;
}
.intro-contact-block-cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}
.intro-contact-section-card {
    max-width: 245px;
    display: inline-block;
    margin-bottom: 30px;
}
</style>