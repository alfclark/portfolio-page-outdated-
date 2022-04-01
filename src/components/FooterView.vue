<template>
  <footer class="footer">
    <img class="footer_logo" src="@/assets/logo.png" alt="logo" />
    <div class="credits">
      <h2 class="by_me">2021 <span>©</span> Handcrafted by me.</h2>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterView",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.footer {
  height: 100%;
  background-color: #783ad6;
  display: flex;
  flex-direction: column;
}

.footer_logo {
  height: 80px;
  width: 80px;
  position: absolute;
  transform: translate(-50%, -50%);
  left: 50%;
}
.by_me {
  text-align: center;
  color: rgba(255, 255, 255, 0.863);
  font-weight: 500;
  font-size: 1rem;
  padding-top: 3rem;
  padding-bottom: 1rem;
  text-decoration: none;
}
</style>
