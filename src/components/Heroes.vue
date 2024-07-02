<template>
  <div class="container col-xxl-8 px-4 py-5" id="home">
    <div class="row flex-lg-row-reverse align-items-center g-5 py-5">
      <div class="container col-10 col-sm-8 col-lg-6">
        <img
          src="../assets/logo-about.png"
          class="d-block mx-lg-auto img-fluid rounded-3"
          alt="Bootstrap Themes"
          width="450"
          height="450"
          loading="lazy"
        />
      </div>
      <div class="col-lg-6">
        <h1 class="display-5 fw-bold lh-1 mb-3" style="color: #57542f">
          Mohammad Irbah Miftakhul Huda
        </h1>
        <h2 :class="textHeroes">
          Bachelor of Information Engineering, <br> Front-End Web Developer, <br> Illustrator.
        </h2>
        <div class="justify-content-md-center">
          <div class="row">
            <div class="col-1"></div>
            <div class="col-10">
              <button
                @click="show = !show"
                type="button"
                class="btn btn-lg px-4 me-md-2 text-white"
                style="background-color: #999558"
              >
                <h5 class="text-white m-2">My Skills</h5>
              </button>
            </div>
            <div class="col-1"></div>
          </div>
          <div class="row">
            <Transition name="tombol">
              <p v-if="show"> 
                <img class="p-3" src="../assets/html-icon.png" alt="logo HTML" width="85" height="85">
                <img class="p-3" src="../assets/css-icon.png" alt="logo CSS" width="80" height="80">
                <img class="p-3" src="../assets/bootstrap-logo.png" alt="logo Bootstrap" width="80" height="80">
                <img class="p-3" src="../assets/SASS-logo.png" alt="logo sass" width="80" height="80">
                <img class="p-3" src="../assets/vue-logo.png" alt="logo Vue.js" width="80" height="80">
                <img class="p-3" src="../assets/vite-logo.png" alt="logo vite" width="80" height="80">
                <img class="p-3" src="../assets/React-logo.png" alt="logo React.js" width="80" height="80">
                <img class="p-3" src="../assets/React Bootstrap-logo.png" alt="logo React-Bootstrap" width="80" height="80">
                <img class="p-3" src="../assets/Material UI-logo.png" alt="logo Material UI" width="80" height="80">
                <img class="p-3" src="../assets/canva-icon.png" alt="logo Canva" width="80" height="80">
              </p>
            </Transition>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.tombol-enter-active,
.tombol-leave-active {
  transition: opacity 1.5s ease;
}

.tombol-enter-from,
.tombol-leave-to {
  opacity: 0;
}
</style>

<script>
export default {
  name: "Heroes",
  data() {
    return {
      show: false,
      textHeroes: "text-dark",
    };
  },
};
</script>
