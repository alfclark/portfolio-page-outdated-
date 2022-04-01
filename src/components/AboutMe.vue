<template>
  <div style="margin-top: -50px; position: absolute" id="about"></div>
  <section class="about">
    <div class="container-about">
      <div class="about-me">
        <div class="this-is-me">
          <h1 class="sub-about">About Me</h1>
          <p class="about-text">
            Hello my name is Alfredo Clark and I am a self-taught Web Developer
            with a passion for making beautiful and responsive web applications
            and websites.
          </p>
          <p class="about-text">
            I like to learn new technologies and use them to deploy better web
            applications.
          </p>
          <p class="about-text">
            Although I use most of my time studying articles and exploring new
            technologies, in my spare time I like to play videogames, cook and
            make music. I also love to share time with my family and friends.
          </p>
        </div>
      </div>
      <div class="social">
        <a class="social-icon" href="https://github.com/alfclark"
          ><i class="fa-brands fa-github"></i
        ></a>
        <a class="social-icon" href="https://www.linkedin.com/in/alfredoclark/"
          ><i class="fa-brands fa-linkedin-in"></i
        ></a>
        <a class="social-icon" href=""><i class="fa-solid fa-file"></i></a>
        <a class="social-icon" href="https://codepen.io/alfclark"
          ><i class="fa-brands fa-codepen"></i
        ></a>
        <a class="social-icon" href="mailto:alfredoclarkcardenas@gmail.com"
          ><i class="fa-solid fa-envelope"></i
        ></a>
      </div>
      <div class="funfact">
        <h3>Fun-Fact Generator About Me:</h3>
        <span class="fact"></span>
        <button>Tell me</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AboutMe",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.about {
  margin: 3rem 0;
}
.container-about {
  background-color: #783ad681;
  text-align: center;
  color: #fff;
  border: #783ad6;
  border-style: solid;
  border-radius: 11px;
  width: 90vw;
  margin: 0 auto;
}
.sub-about {
  font-size: 3rem;
  margin-bottom: 1rem;
  padding-top: 2rem;
}
.about-text {
  font-size: 1.5rem;
  margin: 1rem;
}

.social {
  margin-top: 1rem;
  margin-bottom: 1rem;
}

.social-icon {
  padding: 1rem;
  font-size: 2rem;
  color: #fff;
}

.social-icon:hover {
  color: #141c3a;
}

/* Skills */
.skills {
  max-width: 100%;
  margin-top: 10rem;
  text-align: center;
}

.skill-header {
  margin-bottom: 1rem;
}

.skills-wrapper img {
  padding: 1.25rem;
}

.icon {
  width: 15.875rem;
  height: 15.25rem;
}

.icon:hover {
  animation: shake1 2s ease 0s 1 normal forwards;
}

.icon-card {
  background-color: #fff;
  border-radius: 11px;
  box-shadow: 0 10px 10px #783ad6;
  padding: 20px;
  margin: 10px;
}

.icon-card:hover {
  box-shadow: 0 0;
  border-color: #783ad6;
  border-style: solid;
  border-width: 5px;
}
</style>
