<template>
    <div class="container mx-auto rounded shadow mx-auto">
        <div class="col-md-6 col-12 mx-auto text-center">
            <b-icon icon="megaphone" class="mx-2 text-light my-2" scale="2"></b-icon>
            <h2>Get In Touch</h2>
            <p>I'm always interested in discussing new projects and learning from talented people. Shoot me an email and let's talk about your goals and how I can help you meet them.</p>
            <a class="btn green-btn-two align-items-center mx-auto d-flex w-50 justify-content-center" href="mailto:nathaniel.orona98@gmail.com">Reach Out 
                <b-icon icon="arrow-right" class="mx-2 my-auto"></b-icon>
            </a>
        </div>
    </div>
</template>

<script>
    import { BIcon, BIconArrowRight, BIconMegaphone } from 'bootstrap-vue';
    export default {
        name: 'ContactCTA',

        components: {
            BIcon,
            BIconArrowRight,
            BIconMegaphone
        }
    }
</script>

<style scoped>
.container {
    background-image: linear-gradient(to right, #65238e, #892f8c);
    color: #000;
    margin: 2rem 0;
    padding: 2rem;
    width: 90%;
}

.container::after {
    content: '';
    width: 100%;
    height: 100%;
    left: 0;
    top: 0;
    background: rgba(0, 0, 0, .7);
    z-index: 2;
}

h2 {
    font-weight: bold;
    color: #f2f2f2;
}
</style>