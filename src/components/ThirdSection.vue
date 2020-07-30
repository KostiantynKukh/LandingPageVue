<template>
    <div class="wrap">
        <section class="third-section">
            <div class="third-section-wrapper">
                <h2 class="section-title third-section-title">Light, Fast & Powerful</h2>
                <p class="section-description">
                    Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus 
                    mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.
                </p>                           
            </div>
        </section> 
    </div>
</template>

<script>

export default {
    name: 'ThirdSection'
}

</script>

<style lang="scss" scoped>

.third-section {
    padding: 160px 0;
    background: #fff url('/img/third-block-bg.svg') no-repeat left center;
    display: flex;
    justify-content: flex-end;
}
.third-section-wrapper {
    max-width: 445px;
}
.third-section-title {
    margin-bottom: 16px;
}

</style>
