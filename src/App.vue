<template>
  <NavBar />
  <LandingScreen />
  <AboutMe />
  <FooterView />
</template>

<script>
import NavBar from "./components/NavBar.vue";
import LandingScreen from "./components/LandingScreen.vue";
import AboutMe from "./components/AboutMe.vue";

import FooterView from "./components/FooterView.vue";

export default {
  name: "App",
  components: {
    NavBar,
    LandingScreen,
    AboutMe,
    FooterView,
  },
};
</script>

<style>
/* CUSTOM SCROLLBAR */
::-webkit-scrollbar-track {
  background-color: #141c3a1a;
}

::-webkit-scrollbar {
  width: 12px;
  background-color: #141c3a;
}

::-webkit-scrollbar-thumb {
  background-color: var(--purple);
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
:root {
  --purple: #783ad6;
}
/* ANIMATIONS */
@keyframes bounce1 {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-20px);
  }
  100% {
    transform: translateY(0);
  }
}
@keyframes entrance1 {
  0% {
    animation-timing-function: ease-in;
    opacity: 0;
    transform: translateY(-250px);
  }

  38% {
    animation-timing-function: ease-out;
    opacity: 1;
    transform: translateY(0);
  }

  55% {
    animation-timing-function: ease-in;
    transform: translateY(-65px);
  }

  72% {
    animation-timing-function: ease-out;
    transform: translateY(0);
  }

  81% {
    animation-timing-function: ease-in;
    transform: translateY(-28px);
  }

  90% {
    animation-timing-function: ease-out;
    transform: translateY(0);
  }

  95% {
    animation-timing-function: ease-in;
    transform: translateY(-8px);
  }

  100% {
    animation-timing-function: ease-out;
    transform: translateY(0);
  }
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: white;
  text-align: center;
  background: 50% / contain url(@/assets/universe.png) #141c3a;
}
</style>
