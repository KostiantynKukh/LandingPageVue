<template>
    <div>
        <a v-if='href' :href="href" class="company-logo">Landie</a> 
        <router-link v-else :to="to" class="company-logo">Landie</router-link>                
    </div>  
</template>

<script>
export default {
    name: 'logo-app',
    props: {
        href: {
            type: String,
            required: false
        },
        to: {
            type: String,
            required: false
        },
    }    
}
</script>

<style lang="scss" scoped>
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