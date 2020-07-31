<template>
    <footer class="footer">
            <div class="wrap">

                <div class="top-footer">

                    <span class="top-footer-company">
                        &#169;2020 Yourcompany
                    </span>
                    <router-link to="/" class="company-logo">Landie</router-link> 
                    <w-button type="button" size="md" color="dark">Purchase now</w-button> 

                </div>

                <div class="bottom-footer">

                    <navigation-list />

                    <div class="social-icons">
                        <a href="https://www.facebook.com/" target="_blank" class="facebook social-icon">
                        </a>
                        <a href="https://www.linkedin.com/" target="_blank" class="linkedin social-icon">
                        </a>
                        <a href="https://twitter.com/" target="_blank" class="twitter social-icon">
                        </a>
                        <a href="http://www.youtube.com/" target="_blank" class="youtube social-icon">
                        </a>
                        <a href="https://www.instagram.com/" target="_blank" class="instagram social-icon">
                        </a>
                    </div>

                </div>
            </div>
        </footer>
</template>

<script>
import WButton from "@/widgets/WButton"
import NavigationList from "@/components/NavigationList"

export default {
    name: 'FooterComponent',
    components: {
        WButton,
        NavigationList
    }
}
</script>

<style lang="scss" scoped>

.footer {
    background: #E7ECFF;
    max-width: 1440px;
    margin: 0 auto;
}
.top-footer {
    padding: 67px 0 46px;
    border-bottom: 2px solid #CDD1D4;
    display: flex;
    justify-content: space-between;
}
.top-footer-company {
    font-weight: 500;
    font-size: 1.4em;
    line-height: 24px;
    color: #939EA4;
}
.top-footer-btn {
    max-width: 109px;
    font-weight: 500;
    font-size: 1.2em;
    line-height: 18px;
}
.bottom-footer {
    padding: 20px 0 30px;
    display: flex;
    justify-content: space-between;
}
.footer-nav-link {
    color: #929ECC;
}
.social-icons {
    width: 200px;
    display: flex;
    justify-content: space-between;
}
.social-icon {
    width: 16px;
    height: 16px;
    transform: scale(1);
    transition: 0.2s;

    &:hover {
        transform: scale(2);
    }  
}

.facebook {
    background: url('/img/social-icons/facebook.svg') no-repeat center center;
    background-size: cover;

    &:hover {
        background: url('/img/social-icons/facebook-hover.svg') no-repeat center center;
    }
}

.linkedin {
    background: url('/img/social-icons/linkedin.svg') no-repeat center center;
    background-size: cover;

    &:hover {
        background: url('/img/social-icons/linkedin-hover.svg') no-repeat center center;
    }
}

.twitter {
    background: url('/img/social-icons/twitter.svg') no-repeat center center;
    background-size: cover;

    &:hover {
        background: url('/img/social-icons/twitter-hover.svg') no-repeat center center;
    }
}

.youtube {
    background: url('/img/social-icons/youtube.svg') no-repeat center center;
    background-size: cover;

    &:hover {
        background: url('/img/social-icons/youtube-hover.svg') no-repeat center center;
    }
}

.instagram {
    background: url('/img/social-icons/instagram.svg') no-repeat center center;
    background-size: cover;

    &:hover {
        background: url('/img/social-icons/instagram-hover.svg') no-repeat center center;
    }
}

</style>