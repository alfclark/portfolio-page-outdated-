<template>
  <div id="landing" class="landing">
    <section class="hero">
      <div class="welcome">
        <img class="avatar" src="@/assets/logo.png" />
        <h1 class="my_name">Alfredo Clark</h1>
        <h2 class="job_desc">Web Developer</h2>
        <h3 class="me">
          I am a self-taught web developer. I love coding amazing websites.
        </h3>
        <h3 class="tacos">...and Tacos.</h3>
      </div>
    </section>
    <div class="scroll-me">
      <p class="scroll-text">Don't be shy, scroll through me :)</p>
      <i class="fa-solid fa-arrow-down"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: "LandingScreen",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.landing {
  height: 90vh;
  display: flex;
  flex-direction: column;
  align-content: center;
  justify-content: center;
  position: static;
}
.hero {
  position: relative;
  height: 100%;
  padding-top: 3rem;
}
.avatar {
  width: 20%;
}
.my_name {
  font-size: 3rem;
}
.job_desc {
  font-size: 1.7rem;
  text-decoration: underline;
}
.me {
  font-size: 2rem;
  font-weight: 400;
}
.scroll-me {
  font-size: 1rem;
  text-align: center;
  justify-content: center;
  animation: bounce1 2s infinite, show1 5s forwards;
  position: relative;
  bottom: 0;
  width: 100%;
}
.scroll-text {
  margin: 0;
}
.fa-arrow-down {
  margin-top: -1rem;
}
</style>
