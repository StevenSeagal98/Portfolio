<template>
  <div class="navbar">
  <b-navbar toggleable="lg" type="dark" class="col-12">
    <b-navbar-brand href="#" class="col-1">
      <img src="https://i.imgur.com/Woxg1A1.png" alt="" class="col-10">
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" class="d-flex justify-content-end mx-auto" is-nav>
      <b-navbar-nav class="ml-auto justify-self-end ml-auto">
        <b-nav-item class="link" to="/"><span class="u-bounce">About</span></b-nav-item>
        <b-nav-item class="link" to="/Projects"><span class="u-bounce">Projects</span></b-nav-item>
        <b-nav-item class="link" to="/Projects"><span class="u-bounce">Contact</span></b-nav-item>
      </b-navbar-nav>
      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto socials">
        <b-nav-item>
          <a href="#" class="nav-link">
            <b-icon icon="github"></b-icon>
          </a>
        </b-nav-item>
        <b-nav-item>
          <a href="#" class="nav-link">
            <b-icon icon="linkedin"></b-icon>
          </a>
        </b-nav-item>
          <b-nav-item>
            <a href="mailto:nathaniel.orona98@gmail.com" class="nav-link">
              <b-icon icon="envelope-fill"></b-icon>
            </a>
          </b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
</template>

<script>
  import { BIcon, BIconHouseDoor, BIconLaptop, BIconBook, BIconPhone, BIconLinkedin, BIconGithub, BIconEnvelopeFill } from 'bootstrap-vue';

  export default {
    name: 'Navbar',
    components: {
      BIcon, BIconHouseDoor, BIconLaptop, BIconBook, BIconPhone, BIconGithub, BIconLinkedin, BIconEnvelopeFill
    },
  }
</script>

<style scoped>

  .navbar {
    background: var(--dark-blue);
    height: 10vh;
  }

  .link {
    transition: .2s;
    background: inherit;
    padding: .5rem 1rem;
    animation: all 1s ease;
  }

  .socials * {
    color: #e5e5e5;
  }

  .link a {
    color: #e5e5e5 !important;
    font-size: 1rem;
  }

</style>