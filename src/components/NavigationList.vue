<template>    
        <nav class="nav">                    
            <ul class="nav-list top-nav-list">
                <li class="nav-item"><router-link to="/" class="nav-link top-nav-link">Home</router-link></li>
                <li class="nav-item"><router-link to="/about" class="nav-link top-nav-link">About</router-link></li>
                <li class="nav-item"><router-link to="/contact" class="nav-link top-nav-link">Contact</router-link></li>
            </ul>
        </nav>    
</template>

<script>
export default {
    name: 'NavigationList'    
}
</script>

<style lang="scss" scoped>
.nav {
    width: 245px;    
}
.nav-list {   
    display: flex;
    justify-content: space-between;
}
.nav-link {
    font-size: 1.4em;
    color: #505F98;
    position: relative;
    &:hover {
        color: #14215c;
    }
    &:before {
        content: '';
        width: 0%;
        height: 2px;
        background-color: #14215c;
        position: absolute;
        bottom: 0;
        right: 0;
        transition: 0.3s;
    }
    &:hover:before {
        width: 100%;
        left: 0;
    }
}

</style>