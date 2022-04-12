<template>
  <nav class="navbar sticky-top navbar-expand-lg navbar-dark">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">AC</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link" href="#about">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#skills">Skills</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#projects">Projects</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#contact"
              ><button class="nav-button">Say Hello!</button></a
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.navbar {
  background-color: var(--purple);
  padding: 0.5rem 2rem;
  box-shadow: 0 0 20px #fff;
}
.navbar-brand {
  font-size: 2rem;
  font-weight: 600;
}
.navbar-nav {
  align-items: center;
}
.nav-link {
  color: white;
  font-weight: 500;
  font-size: 1.2rem;
  margin: 0 0.5rem;
}
.nav-link:hover {
  text-decoration: underline;
}
.nav-button {
  text-decoration: none;
  color: #fff;
  font-size: 1.2rem;
  padding: 0.5rem 1.5rem;
  background-color: transparent;
  border: none;
  border: solid;
  border-radius: 2.2rem;
}
.nav-button:hover {
  background-color: #141c3a;
  transition: 0.4s;
}
</style>
