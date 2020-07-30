<template>
    <div class="wrap">
        <section class="intro">
            <div class="intro-wrap">
                <h1 class="intro-title">
                    Introduce Your Product Quickly & Effectively
                </h1>
                <p class="intro-desc">
                    Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus 
                    mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.
                </p>
                <W-button class="intro-btn" size="lg" color="dark">
                    Purchase UI Kit
                </W-button>
                <W-button size="lg" color="light">
                    Learn More
                </W-button>
            </div>
        </section> 
    </div>
</template>

<script>
import WButton from '@/widgets/WButton'

export default {
    name: "Intro",
    components: {
        WButton        
    }
}
</script>

<style lang="scss" scoped>
.intro {
    padding: 250px 0 380px;
}
.intro-wrap {
    max-width: 540px;
}
.intro-title {
    margin-bottom: 20px;
    font-weight: 500;
    font-size: 5em;
    line-height: 66px;
    letter-spacing: 1px;
    color: #091133;
}
.intro-desc {
    margin-bottom: 69px;
    font-size: 18px;
    line-height: 30px;
    color: #505F98;   
}
.intro-btn {
    margin-right: 30px;
}
</style>