<template>
    <div class="container-fluid px-0">
        <Navbar />
        <ProjectsNew />
        <ContactCTA />
        <Footer />
    </div>
</template>

<script>
    export default {
        name: 'Projects',

        components: {

        },

        data() {
            return {

            }
        }
    }
</script>

<style scoped>
.container-fluid {
    background: var(--dark-blue);
}
</style>