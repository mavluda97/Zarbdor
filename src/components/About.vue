<template>
  <div class="px-10 pt-16 pb-0" id="about">
    <h1 class="text-uppercase headline font-weight-bold ma-6" style="color: #19d3cc">
      {{ $t("Loyiha haqida") }}
    </h1>
    <div class="about-container">
      <p class="mx-5 mt-15 about-p-style" style="color: #3d3d3d">
        {{ $t("About-definition") }}
      </p>
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
  padding: 20px;
  padding-top: 0;
  background-color: #e5e5e5;
  display: grid;
  grid-template-columns: minmax(100px, 1000px) auto;
  grid-template-rows: 800px;
  justify-content: start;
  column-gap: 100px;
}

.about-p-style {
  font-size: 20px;
}

.about-image {
  height: 100%;
  width: 100%;
}

@media (min-width: 2000px) {
  .about-container {
    justify-content: space-around;
  }
}

@media (max-width: 1300px) {
  .about-container {
    display: flex;
    flex-direction: column;
    row-gap: 20px;
  }
  .about-image {
    margin: 0 auto;
    height: 50%;
    width: 50%;
  }
}

@media (max-width: 520px) {
  .about-p-style {
    font-size: 16px;
  }
}
</style>
