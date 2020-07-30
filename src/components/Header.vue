<template>
    <div class="wrap">
        <header class="header">            
                <navigation-list />
                <router-link to="/" class="company-logo">Landie</router-link> 
                <w-button type="button" size="md" color="dark">Buy Now</w-button>              
        </header>        
    </div>   
</template>

<script>
import WButton from '@/widgets/WButton'
import NavigationList from '@/components/NavigationList'

export default {
    name: 'HeaderMain',
    components: {
        WButton,        
        NavigationList
    }    
}
</script>
<style lang="scss">
.header {
    width: 100%;
    display: flex;
    justify-content: space-between;
    padding: 16px 0;   
    align-items: center;
    z-index: 3;
}
.company-logo {
    font-weight: 900;
    font-size: 2.6em;
    color: #37447E;
    transition: 0.2s;
    cursor: pointer;

    &:hover {
    color: rgb(255, 0, 212);
    }    
}
</style>