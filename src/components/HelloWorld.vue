<template>
  <div class="hello">
    <!-- <Navbar @goTo="handleNavigation" />
    <transition name="fade">
      <Heroes v-if="currentSection === 'home'" />
    </transition>
    <transition name="fade">
      <About v-if="currentSection === 'about'" />
    </transition>
    <transition name="fade">
      <Form v-if="currentSection === 'contact'" />
    </transition> -->
    <Navbar />
    <Heroes />
    <About />
    <Portfolio />
    <Form />
    <Footer />
  </div>
</template>

<script>
import Navbar from "./Navbar.vue";
import Heroes from "./Heroes.vue";
import About from "./About.vue";
import Portfolio from "./Portfolio.vue";
import Form from "./Form.vue";
import Footer from "./Footer.vue";

export default {
  name: "HelloWorld",
  components: {
    Navbar,
    Heroes,
    About,
    Portfolio,
    Form,
    Footer,
  },
  // data() {
  //   return {
  //     currentSection: "home",
  //   };
  // },
  // methods: {
  //   handleNavigation(section) {
  //     this.currentSection = section;
  //   },
  // },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: black;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active di <2.1.8 */ {
  opacity: 0;
}

/* Form */
.small-form {
  max-width: 650px;
  margin: 0 auto;
}

.small-form .container {
  padding: 10px;
}

.small-form .form-control {
  font-size: 14px;
}

.small-form .btn {
  font-size: 14px;
  padding: 5px 10px;
}

/* Portfolio */
/* Menyesuaikan ukuran kartu */
.small-card .card {
  width: 50;
  height: 50px;
}

/* Menambahkan gaya agar kartu memiliki tinggi yang sama */
.small-card .card-body {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.small-card .btn a {
  color: #ffffff;
  text-decoration: none;
}

@media (max-width: 600px) {
  div.portfolio {
    width: 100%;
    margin-bottom: 30px;
    background-color: whitesmoke;
  }
}
</style>
