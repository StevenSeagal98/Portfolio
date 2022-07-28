<template>
  <!--<div class="navbar">
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
</div>-->
<div>
  <b-navbar toggleable="lg" type="dark">
    <b-navbar-brand to="/" class="col-4 col-md-2">
      <img src="https://i.imgur.com/Woxg1A1.png" alt="Nate Orona Logo" class="col-10 col-md-4 mx-auto">
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" class="col-md-7 col-12 ml-auto" is-nav>
      <b-navbar-nav>
        <b-nav-item to="/" class="u-bounce mx-2">Home</b-nav-item>
        <b-nav-item to="/About" class="u-bounce mx-2">About</b-nav-item>
        <b-nav-item to="/projects" class="u-bounce mx-2">Projects</b-nav-item>
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

  #nav-collapse {
    z-index: 1000;
    background: var(--dark-blue);
  }
  .navbar {
    background: var(--dark-blue);
    width: 100%;
  }

  .icon {
    color: var(--primary-light);
    transition: all .2s;
  }

</style>