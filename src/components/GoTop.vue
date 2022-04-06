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
  right: 5%;
  bottom: 5%;
  cursor: pointer;
  animation: bounce1 5s infinite;
  color: #fff;
  font-size: 2rem;
  z-index: 3;
}
@media screen and (max-width: 900px) {
}
</style>
