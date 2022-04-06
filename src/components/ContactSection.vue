<template>
  <div style="margin-top: -50px; position: absolute" id="contact"></div>
  <section class="contact">
    <div class="animation">
      <span>hello</span>
    </div>
    <div class="form">
      <form
        ref="anyName"
        @submit="submitForm"
        action="https://formsubmit.co/alfredoclarkcardenas@gmail.com"
        method="POST"
      >
        <input type="hidden" name="_captcha" value="false" />
        <input type="text" name="name" placeholder="Your Name" required />
        <input type="hidden" name="_next" value="http://localhost:8080/" />
        <input type="hidden" name="_template" value="table" />
        <input
          type="email"
          name="email"
          placeholder="your@email.com"
          required
        />
        <label for="reason">I'm contacting you because:</label>
        <select name="reason" id="reason">
          <option value="none"></option>
          <option value="professional">Professional reasons</option>
          <option value="education">Education</option>
          <option value="feedback">Feedback</option>
          <option value="charity">Charity or social activities</option>
          <option value="starWars">Chat about Star Wars</option>
          <option value="other">Other</option>
        </select>
        <input type="text" name="message" placeholder="Your Message" required />
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
  align-items: center;
  justify-content: center;
  padding: 0;
  margin: 3rem 0;
}
.animation {
  background-color: aqua;
  width: 40vw;
  height: 100%;
}
.form form {
  width: 40vw;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
input,
label {
  margin-top: 1rem;
}
input,
label,
select {
  width: 90%;
}
.button {
  margin: 1rem 0;
  padding: 0.5rem 3rem;
  background-color: transparent;
  color: var(--purple);
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
}
</style>
