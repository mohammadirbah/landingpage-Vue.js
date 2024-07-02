<template>
  <div
    class="text-secondary px-4 py-5 text-center"
    style="background-color: #999558"
    id="about"
  >
    <div class="py-5">
      <div
        class="container d-flex align-items-center justify-content-center flex-column flex-lg-row"
      >
        <div class="col-lg-6 d-flex justify-content-center mb-4 mb-lg-0">
          <img
            src="../assets/foto_profile_baru.png"
            class="img-fluid rounded-3"
            alt="Bootstrap Themes"
            width="450"
            height="450"
            loading="lazy"
          />
        </div>
        <div class="col-lg-6 mx-auto">
          <h1 class="display-5 fw-bold text-white">About Me</h1>
          <p :class="textAbout">
            Hello, I am a Bachelor of Information Engineering who has an
            understanding of software development, hardware, and information
            technology. I'm a website design enthusiast, with expertise in HTML,
            CSS, Bootstrap, Vue.js, React.js, React-Bootstrap, and Material UI.
            I believe that good design is the key to great user experience, and
            I am dedicated to creating aesthetically pleasing and functional
            interfaces. With the experience I have, I have honed my skills in
            building responsive and engaging websites. I am always looking for
            new challenges to develop my skills and contribute to a dynamic
            team.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "About",
      textAbout: "text-dark",
    };
  },
};
</script>

<style>
@media (max-width: 991px) {
  .d-flex .mb-4 {
    margin-bottom: 1.5rem !important;
  }
}
</style>
