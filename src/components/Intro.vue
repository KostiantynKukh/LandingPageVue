<template>
    <div class="wrap">
        <section class="intro">
            <div class="intro-wrap">
                <intro-title class="intro-title"></intro-title>
                <intro-desc class="intro-desc"></intro-desc>
                <Wbutton class="intro-btn" size="lg" color="dark">
                    Purchase UI Kit
                </Wbutton>
                <Wbutton size="lg" color="light">
                    Learn More
                </Wbutton>
            </div>
        </section> 
    </div>
</template>

<script>
import Wbutton from '../widgets/button/Wbutton'
import IntroTitle from '../widgets/introW/IntroTitle'
import IntroDesc from '../widgets/introW/IntroDesc'
export default {
    name: "intro",
    components: {
        Wbutton,
        IntroTitle,
        IntroDesc
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
}
.intro-desc {
    margin-bottom: 69px;
}
.intro-btn {
    margin-right: 30px;
}
</style>