<template>
    <footer class="footer py-2 d-flex flex-row col-12 align-items-center">
        <p class="mx-auto my-auto">Made With <b-icon icon="heart" variant="danger" class="icon"></b-icon> By <span class="gr-text">Nate Orona</span></p>
    </footer>
</template>

<script>
    import { BIcon, BIconHeart } from 'bootstrap-vue';
    export default {
        name: 'Footer',
        components: {
            BIcon,
            BIconHeart
        }
    }
</script>

<style scoped>
    footer {
        background: #121212;
        color: var(--primary-light);
        margin: 0 auto;
        height: 10vh;
    }

    .icon {
        margin: 0 .5rem;
    }
</style>