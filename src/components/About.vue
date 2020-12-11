<template>
  <div class="about-container" id="about">
    <div class="ma-10">
      <h1 class="text-uppercase headline font-weight-bold ma-5" style="color: #19d3cc">
        {{ $t("Loyiha haqida") }}
      </h1>
      <p class="mx-5 mt-15 headline" style="color: #3d3d3d">
        {{ $t("About-definition") }}
      </p>
    </div>
    <div class="ma-15 d-flex justify-center">
      <img src="../assets/only.png" alt="pic" class="about-image" />
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
};
</script>

<style scoped>
.about-container {
  width: 100%;
  background-color: #e5e5e5;
  display: grid;
  grid-template-columns: auto auto;
}

.about-image {
  height: 100%;
  width: 100%;
}

@media (max-width: 1000px) {
  .about-container {
    grid-template-columns: auto;
    grid-template-rows: auto auto;
    justify-content: center;
  }

  .about-image {
    height: 85%;
    width: 50%;
  }
}

@media (max-width: 560px) {
  .about-image {
    height: 100%;
    width: 100%;
  }
}
</style>
