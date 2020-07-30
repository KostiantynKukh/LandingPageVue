<template>
    <div class="wrap">
        <section class="second-section">
            <div class="second-section-wrapper">
                <h2 class="section-title second-section-title">Light, Fast & Powerful</h2>
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
    name: 'SecondSection'    
}
</script>

<style lang="scss" scoped>
.second-section {
    padding: 160px 0;
    background: #fff url('/img/second-block-bg.svg') no-repeat left center;
    display: flex;
    justify-content: flex-end;
}
.second-section-wrapper {
    max-width: 445px;
}
.second-section-title {
    margin-bottom: 16px;
}
</style>
