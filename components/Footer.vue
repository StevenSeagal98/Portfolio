<template>
    <footer class="footer py-2 d-flex flex-row col-12">
        <div class="container d-flex flex-row flex-wrap justify-content-between">
            <div class="text col-12 col-md-4 justify-content-center d-flex align-items-center">
                <p class="my-auto footer-text">
                    Made With 
                    <b-icon icon="heart" variant="danger" class="icon"></b-icon> 
                    By 
                    <span class="gr-text">Nate Orona</span>
                </p>
            </div>
            <div class="social-links d-flex flex-row justify-content-around col-12 col-md-4">
                <a href="mailto:nathaniel.orona98@gmail.com" target="_blank">
                    <b-icon icon="envelope-fill" scale="1.5"></b-icon>
                </a>
                <a href="https://www.linkedin.com/in/nate-o-27806b102/" target="_blank">
                    <b-icon icon="linkedin" scale="1.5"></b-icon>
                </a>
                <a href="https://github.com/StevenSeagal98" target="_blank">
                    <b-icon icon="github" scale="1.5"></b-icon>
                </a>
                
            </div>
        </div>
    </footer>
</template>

<script>
    import { BIcon, BIconHeart, BIconGithub, BIconLinkedin, BIconEnvelopeFill } from 'bootstrap-vue';
    export default {
        name: 'Footer',
        components: {
            BIcon,
            BIconHeart,
            BIconEnvelopeFill,
            BIconGithub,
            BIconLinkedin
        }
    }
</script>

<style scoped>
    footer {
        background: #121212;
        color: var(--primary-light);
        margin: 0 auto;
    }

    .footer-text {
        font-size: .9em;
    }

    .icon {
        margin: 0 .3rem;
    }

    .text, .social-links {
        width: fit-content;
    }

    .social-links a {
        margin: 0 1rem;
        padding: .5rem;
    }
</style>