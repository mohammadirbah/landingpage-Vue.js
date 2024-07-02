<template>
  <nav
    class="navbar navbar-expand-md navbar-dark fixed-top"
    style="background-color: #2f2d17"
  >
    <div class="container-fluid">
      <!-- <a @click="goTo('home')" class="navbar-brand text-grey" href="#home">
        <img
          src="../assets/foto-profil.jpeg" 
          alt="Foto Profil"
          class="rounded-circle"
          style="max-width: 7vh"
      /></a> -->
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarCollapse"
        aria-controls="navbarCollapse"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarCollapse">
        <ul class="navbar-nav mx-auto mb-2 mb-md-0">
          <!-- <transition>
            <li class="nav-item">
              <a @click="goTo('about')" class="nav-link"> About</a>
            </li>
          </transition>
          <transition>
            <li class="nav-item">
              <a @click="goTo('portfolio')" class="nav-link"> Portfolio</a>
            </li>
          </transition>
          <transition>
            <li class="nav-item">
              <a @click="goTo('contact')" class="nav-link"> Contact</a>
            </li>
          </transition> -->
          <li class="nav-item">
            <a href="#home" class="nav-link" style="color: white"> Home</a>
          </li>
          <li class="nav-item">
            <a href="#about" class="nav-link" style="color: white"> About</a>
          </li>
          <li class="nav-item">
            <a href="#portfolio" class="nav-link" style="color: white"> Portfolio</a>
          </li>
          <li class="nav-item">
            <a href="#contact" class="nav-link" style="color: white"> Contact</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  methods: {
    goTo(section) {
      this.$emit("goTo", section);
    },
  },
};
</script>

<style scoped>
/* CSS untuk transisi */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active di <2.1.8 */ {
  opacity: 0;
}
</style>
