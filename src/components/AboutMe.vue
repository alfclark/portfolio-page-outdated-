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
        <a
          class="social-icon"
          href="https://github.com/alfclark"
          target="_blank"
          ><i class="fa-brands fa-github"></i
        ></a>
        <a
          class="social-icon"
          href="https://www.linkedin.com/in/alfredoclark/"
          target="_blank"
          ><i class="fa-brands fa-linkedin-in"></i
        ></a>
        <a class="social-icon" href=""><i class="fa-solid fa-file"></i></a>
        <a
          class="social-icon"
          href="https://codepen.io/alfclark"
          target="_blank"
          ><i class="fa-brands fa-codepen"></i
        ></a>
        <a
          class="social-icon"
          href="mailto:alfredoclarkcardenas@gmail.com"
          target="_blank"
          ><i class="fa-solid fa-envelope"></i
        ></a>
      </div>
      <div class="funfact">
        <h2>Want to know more about me?</h2>
        <button class="factButton" @click="generateFact">Tell me</button>
        <p class="fact">{{ fact }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    generateFact() {
      const numSelect = Math.floor(Math.random() * this.facts.length);
      this.fact = this.facts[numSelect];
    },
  },
  data() {
    return {
      fact: "",
      facts: [
        "🐉 I lived 2 years in China 🐉",
        "🎹 I play 6 instruments 🎹",
        "👽 I am a big Star Wars fan 👽",
        "🚗 I used to work for a Car Maker 🚗",
        "💼 I used to have a small trade company 💼",
        "⚽ I have played soccer for more than 15 years ⚽",
        "🐾 I have 2 dogs 🐾",
        "🥡 My chinese name is 马超 🥡",
        "🏃🏻‍♂️ I have a national silver medal in track & field 🏃🏻‍♂️",
        "🤖 I am a Mechatronics Engineer 🤖",
        "🚀 My favourite videogame is Rocket League 🚀",
        "🤓 I won a full scholarship for post-graduate studies in China 🤓",
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.about {
  margin-top: 3rem;
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
  padding: 3rem 0;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.sub-about {
  font-size: 3rem;
  margin-bottom: 1rem;
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
  transition: 0.4s;
}
.funfact {
  background-color: rgba(255, 255, 255, 0.813);
  color: var(--purple);
  width: 70%;
  border-radius: 1rem;
  padding: 1rem;
}
.funfact h2 {
  text-decoration: underline;
  font-weight: 600;
}
.factButton {
  border: none;
  background-color: var(--purple);
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 1.5rem;
  margin: 0.5rem;
}
.factButton:hover {
  background-color: var(--dark);
  color: white;
  transition: 0.4s;
}
.fact {
  font-size: 1.5rem;
  color: var(--dark);
}
@media screen and (max-width: 900px) {
  .sub-about {
    font-size: 2rem;
  }
  .about-text {
    font-size: 1rem;
  }
  .social-icon {
    font-size: 1.5rem;
  }
  .funfact h2 {
    font-size: 1.5rem;
  }
  .fact {
    font-size: 1rem;
  }
}
</style>
