<template>
  <div style="margin-top: -80px; position: absolute" id="projects"></div>
  <section class="container">
    <div class="projects">
      <h1 class="subtitle">
        My Recent Projects
        <hr class="divider" />
      </h1>
      <div class="projects-wrapper">
        <div
          class="project project-tile"
          :class="cardSelected"
          @click="selected"
        >
          <div class="img">
            <img
              class="project-image"
              src="@/assets/projects/GameZone.png"
              alt="project"
              :class="onSelection"
            />
            <div class="links" :class="isShown">
              <a class="link" href=""
                ><i class="fa-solid fa-up-right-from-square"></i
              ></a>
              |
              <a class="link" href=""><i class="fa-brands fa-github"></i></a>
            </div>
          </div>
          <div class="card-title">
            <p class="project-title">
              <span class="code">&lt;</span>
              Game Zone
              <span class="code">&#47;&gt;</span>
            </p>
            <div class="technologies">
              <i class="fa-brands fa-vuejs"></i>
              <i class="fa-brands fa-css3-alt"></i>
              <i class="fa-brands fa-html5"></i>
              <i class="fa-brands fa-js"></i>
              <i class="fa-brands fa-bootstrap"></i>
            </div>
          </div>
        </div>
        <div
          class="project project-tile"
          :class="cardSelected"
          @click="selected"
        >
          <div class="img">
            <img
              class="project-image"
              src="https://cdn.freecodecamp.org/testable-projects-fcc/images/random-quote-machine.png"
              alt="project"
              :class="onSelection"
            />
            <div class="links" :class="isShown">
              <a class="link" href="https://alfclark-gamezone.netlify.app/"
                ><i class="fa-solid fa-up-right-from-square"></i
              ></a>
              |
              <a class="link" href="https://github.com/alfclark/game-zone"
                ><i class="fa-brands fa-github"></i
              ></a>
            </div>
          </div>
          <div class="card-title">
            <p class="project-title">
              <span class="code">&lt;</span>
              Rock, Paper, Scissors
              <span class="code">&#47;&gt;</span>
            </p>
            <div class="technologies">
              <i class="fa-brands fa-css3-alt"></i>
              <i class="fa-brands fa-html5"></i>
              <i class="fa-brands fa-js"></i>
            </div>
          </div>
        </div>
        <div
          class="project project-tile"
          :class="cardSelected"
          @click="selected"
        >
          <div class="img">
            <img
              class="project-image"
              src="https://cdn.freecodecamp.org/testable-projects-fcc/images/random-quote-machine.png"
              alt="project"
              :class="onSelection"
            />
            <div class="links" :class="isShown">
              <a class="link" href=""
                ><i class="fa-solid fa-up-right-from-square"></i
              ></a>
              |
              <a class="link" href=""><i class="fa-brands fa-github"></i></a>
            </div>
          </div>
          <div class="card-title">
            <p class="project-title">
              <span class="code">&lt;</span>
              Rock, Paper, Scissors
              <span class="code">&#47;&gt;</span>
            </p>
            <div class="technologies">
              <i class="fa-brands fa-css3-alt"></i>
              <i class="fa-brands fa-html5"></i>
              <i class="fa-brands fa-js"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    selected() {
      const cardStatus = "selected";
      const imgStatus = "isSelected";
      const linkStatus = "isShown";
      if (this.cardSelected === "") {
        this.cardSelected = cardStatus;
        this.onSelection = imgStatus;
        this.isShown = linkStatus;
      } else {
        this.cardSelected = "";
        this.onSelection = "";
        this.isShown = "";
      }
    },
  },
  data() {
    return {
      cardSelected: "",
      onSelection: "",
      isShown: "",
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  width: 90vw;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 4rem;
}
.projects {
  width: 80vw;
  display: flex;
  flex-direction: column;
  text-align: center;
  justify-content: center;
}
.projects-wrapper {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  width: 80vw;
}
.project {
  background: #783ad6;
  border-radius: 11px;
  transition: 0.3s;
  text-decoration: none;
  width: 20rem;
  height: 25rem;
  cursor: pointer;
  margin: 2rem;
}
.project:hover {
  background-color: #141c3a;
}
.img {
  height: 90%;
  margin: 0;
  padding: 0;
}
.project-image {
  object-fit: cover;
  width: 100%;
  border-radius: 11px 11px 0 0;
  height: 90%;
}
.links {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
  display: flex;
  width: 5rem;
  justify-content: space-around;
  gap: 2rem;
  font-size: 2rem;
  display: none;
}
.link {
  color: white;
}
.link:hover {
  color: var(--dark);
  transition: 0.4s;
}
.card-title {
  margin-top: -1.2rem;
  padding: 0;
}
.project-title {
  font-size: 1rem;
  font-weight: 400;
  text-decoration: none;
  margin: 0;
}
.code {
  color: transparent;
  transition: color 0.3s ease-out;
}
.project:hover .code {
  color: #ff7f50;
  text-decoration: underline;
}
.technologies {
  display: flex;
  gap: 0.5rem;
  align-items: center;
  justify-content: center;
}
.technologies .fa-brands {
  margin-top: 0.5rem;
  color: white;
  font-size: 1.3rem;
}
.project:hover .project-title {
  color: #ff7f50;
  text-decoration: underline;
}
.project:hover .technologies .fa-brands {
  color: #ff7f50;
}
.selected {
  transform: scale(1.05);
}
.isSelected {
  opacity: 30%;
  transition: 0.4s;
}
.isShown {
  display: flex;
  transition: 0.4s;
}
@media screen and (max-width: 900px) {
  .projects {
    width: 95vw;
  }
  .projects-wrapper {
    width: 95vw;
  }
  .project {
    width: 10rem;
    height: 15rem;
    margin: 0.7rem;
  }
  .project-title {
    font-size: 0.7rem;
  }
  .technologies .fa-brands {
    font-size: 0.7rem;
  }
}
</style>
