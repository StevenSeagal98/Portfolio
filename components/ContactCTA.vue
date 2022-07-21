<template>
    <div class="container mx-auto rounded shadow">
        <div class="col-md-6 col-12 mx-auto text-center">
            <h2>Get In Touch <b-icon icon="megaphone" class="mx-2"></b-icon></h2>
            <p>I'm always interested in discussing new projects and learning from talented people. Shoot me an email and let's talk about your goals and how I can help you meet them.</p>
            <button class="btn green-btn-two align-items-center mx-auto d-flex">Reach Out 
                <b-icon icon="arrow-right" class="mx-2 my-auto"></b-icon>
            </button>
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
    background-image: linear-gradient(to right, var(--light-purple), #bb48bf);
    color: #000;
    margin: 2rem 0;
    padding: 2rem;
}

h2 {
    font-weight: bold;
    color: #121212;
}
</style>