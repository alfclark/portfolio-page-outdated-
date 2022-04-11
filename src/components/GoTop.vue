<template>
  <i @click="goTop" class="fa-solid fa-arrow-up"></i>
</template>

<script>
export default {
  methods: {
    goTop() {
      window.scrollTo({
        top: 0,
        left: 0,
        behavior: "smooth",
      });
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.fa-arrow-up {
  position: fixed;
  right: 3%;
  bottom: 3%;
  cursor: pointer;
  animation: bounce1 5s infinite;
  color: #fff;
  font-size: 2rem;
  z-index: 3;
  background-color: var(--purple);
  padding: 0.3rem 0.5rem;
  border-radius: 50%;
}
.fa-arrow-up:hover {
  background-color: var(--dark);
  transition: 0.4s;
}
@media screen and (max-width: 900px) {
  .fa-arrow-up {
    font-size: 1.5rem;
    right: 7%;
    bottom: 3%;
  }
}
</style>
