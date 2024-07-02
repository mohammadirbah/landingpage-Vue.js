<template>
  <form class="p-5 small-form" @submit.prevent="sendEmail">
    <div class="card mt-5 container" style="background-color: #999558">
      <div class="container" id="contact">
        <h1 class="text-center text-white p-5">
          <strong>Contact Me</strong>
        </h1>
        <div class="mb-3 text-start">
          <label for="name" class="form-label text-start text-white">
            Name:
          </label>
          <input
            type="text"
            class="form-control"
            id="name"
            v-model="form.name"
            required
          />
        </div>
      </div>
      <div class="container">
        <div class="mb-3 text-start">
          <label for="email" class="form-label text-start text-white">
            Email:
          </label>
          <input
            type="email"
            class="form-control"
            id="email"
            v-model="form.email"
            required
          />
        </div>
      </div>
      <div class="container">
        <div class="mb-3 text-start">
          <label for="message" class="form-label text-start text-white">
            Message:
          </label>
          <textarea
            id="message"
            class="form-control"
            rows="3"
            v-model="form.message"
            required
          ></textarea>
        </div>
      </div>
      <div class="container">
        <button type="submit" class="btn mb-4 text-white" style="background-color: #57542f">
          Submit
        </button>
      </div>
    </div>
  </form>
</template>

<script>
import emailjs from 'emailjs-com';

export default {
  name: "Form",
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      }
    };
  },
  methods: {
    sendEmail() {
      const serviceID = 'service_lsas6as';
      const templateID = 'template_fxfshgs';
      const userID = 'HEiVr5nkIfAKV626e';

      const templateParams = {
        name: this.form.name,
        email: this.form.email,
        message: this.form.message
      };

      emailjs.send(serviceID, templateID, templateParams, userID)
        .then((response) => {
          console.log('SUCCESS!', response.status, response.text);
          alert('Your message has been sent successfully!');
          this.form.name = '';
          this.form.email = '';
          this.form.message = '';
        }, (error) => {
          console.error('FAILED...', error);
          alert('There was an error sending your message. Please try again.');
        });
    }
  }
};
</script>
