<template>
  <!-- Skills Section -->
  <section id="skills" class="container">
    <div class="skills">
      <h1 class="subtitle">
        My Top Skills
        <hr class="divider" />
      </h1>
      <div class="skills-wrapper">
        <div class="first-set animate__animated animate__pulse">
          <img
            src="@/assets/icons8-javascript.svg"
            alt=""
            loading="lazy"
            class="icon icon-card"
          />
          <img
            src="@/assets/icons8-html-5.svg"
            alt=""
            loading="lazy"
            class="icon icon-card"
          />
          <img
            src="@/assets/icons8-css3.svg"
            alt=""
            loading="lazy"
            class="icon icon-card"
          />
          <img
            src="@/assets/icons8-vue.svg"
            alt=""
            loading="lazy"
            class="icon icon-card"
          />
        </div>

        <div class="second-set animate__animated animate__pulse">
          <img
            src="@/assets/icons8-python.svg"
            alt=""
            loading="lazy"
            class="icon icon-card"
          />
          <img
            src="@/assets/icons8-git.svg"
            alt=""
            loading="lazy"
            class="icon icon-card"
          />
          <img
            src="@/assets/icons8-bootstrap.svg"
            alt=""
            loading="lazy"
            class="icon icon-card"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.skills {
  max-width: 100%;
  margin-top: 4rem;
  text-align: center;
}

.skill-header {
  margin-bottom: 1rem;
}

.skills-wrapper img {
  padding: 1.25rem;
}

.icon {
  width: 10rem;
  height: 10rem;
}

.icon:hover {
  animation: shake1 2s ease 0s 1 normal forwards;
}

.icon-card {
  background-color: #fff;
  border-radius: 11px;
  box-shadow: 0 10px 10px #783ad6;
  margin: 1rem;
}

.icon-card:hover {
  box-shadow: 0 0;
  border-color: #783ad6;
  border-style: solid;
  border-width: 5px;
}
</style>
