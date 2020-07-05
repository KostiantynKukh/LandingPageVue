<template>
    <div class="wrap">
        <header class="header">            
                <Nav></Nav>
                <logo to='/'>Landie</logo>
                <Wbutton type="button" size="md" color="dark">Buy Now</Wbutton>              
        </header>        
    </div>   
</template>

<script>
import Wbutton from '../widgets/button/Wbutton'
import Logo from '../widgets/logo/Logo'
import Nav from '../components/Nav'

export default {
    name: 'header-app',
    components: {
        Wbutton,
        Logo,
        Nav
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
</style>