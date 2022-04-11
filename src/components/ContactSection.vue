<template>
  <div style="margin-top: -50px; position: absolute" id="contact"></div>
  <section class="contact">
    <div class="animation">
      <h3>Get in touch — let’s work together!</h3>
    </div>
    <div class="form">
      <form
        class="row g-3"
        ref="anyName"
        @submit="submitForm"
        autocomplete="off"
        action="https://formsubmit.co/9144a6a93c855ef6560bfe2b18cdbc55"
        method="POST"
      >
        <!-- Configs -->
        <input type="text" name="_honey" style="display: none" />
        <input type="hidden" name="_captcha" value="false" />
        <input
          type="hidden"
          name="_next"
          value="https://www.alfclark.dev/#contact"
        />
        <input
          type="hidden"
          name="_subject"
          value="New message from portfolio page!"
        />
        <!-- Inputs -->
        <input
          type="text"
          name="name"
          v-model="name"
          placeholder="What's your name?"
          required
        />
        <input
          type="email"
          name="email"
          v-model="email"
          placeholder="your@email.com"
          required
        />
        <label for="reason">I'm contacting you because:</label>
        <select name="reason" v-model="reason">
          <option value="" disabled selected>Select reason</option>
          <option value="professional">Professional reasons</option>
          <option value="education">Education</option>
          <option value="feedback">Feedback</option>
          <option value="charity">Charity or social activities</option>
          <option value="starWars">Chat about Star Wars</option>
          <option value="other">Other</option>
        </select>
        <input
          type="text"
          name="message"
          v-model="message"
          placeholder="Your Message"
          required
          cols="30"
          rows="5"
        />
        <button class="button" :class="hide" type="submit">Submit</button>
        <div class="sent" :class="show">
          Sent! <i class="fa-solid fa-check"></i>
        </div>
      </form>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    submitForm() {
      this.$refs.anyName.reset();
      const btnStatus = "hide";
      const sentStatus = "show";
      this.hide = btnStatus;
      this.show = sentStatus;
    },
  },
  data() {
    return {
      hide: "",
      show: "",
    };
  },
};
</script>

<style scoped>
.contact {
  display: flex;
  height: 100%;
  padding: 0;
  margin: 3rem 0;
  left: 0;
}
.animation {
  display: flex;
  flex-direction: column;
  position: relative;
  width: 30vw;
  height: 100%;
}

.form form {
  width: 70vw;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 0 2rem;
}

label {
  margin-top: 1rem;
}
input,
select {
  margin-top: 1rem;
  height: 65px;
  width: 100%;
  border: 2px solid var(--purple);
  background: var(--dark);
  padding: 0 1.5rem;
  border-radius: 15px;
  outline: none;
  font-weight: 400;
  font-size: 1rem;
  color: white;
}

::placeholder {
  color: rgba(212, 212, 212, 0.176);
}

.button {
  margin: 1rem 0;
  padding: 0.5rem 3rem;
  background-color: var(--dark);
  color: white;
  border: solid var(--purple);
  border-radius: 2rem;
}
.button:hover {
  background-color: var(--purple);
  color: white;
  transition: 0.4s;
}
.sent {
  margin: 1rem 0;
  padding: 0.5rem 3rem;
  background-color: rgb(64, 134, 64);
  color: white;
  border: solid rgb(64, 134, 64);
  border-radius: 2rem;
  display: none;
}
.hide {
  display: none;
  transition: 1s;
}
.show {
  display: block;
  transition: 1s;
}

@media screen and (max-width: 900px) {
  .contact {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .animation {
    width: 100vw;
  }
}
</style>
