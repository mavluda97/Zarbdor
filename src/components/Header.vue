<template>
  <div class="header-container pa-15" id="main">
    <div class="ma-15 d-flex justify-end">
      <img
        src="../assets/only.png"
        alt="pic"
        height="100%"
        width="100%"
        class="header-picture"
      />
    </div>
    <div class="my-10">
      <h1
        class="white--text font-weight-bold h1-style"
        style="position: relative; z-index: 33"
      >
        <span class="text-uppercase">Obod-zarbdor</span><br />
        loyihasi
      </h1>
      <p
        style="color: #2b85c5; position: relative; z-index: 32"
        class="mt-10 mb-10 p-style"
      >
        Sizning muammo va takliflaringizni Zarbdor tuman hokimiyatiga yetkazishga va uning
        yechimini topishga mo’ljallangan
      </p>
      <v-btn
        style="position: relative; z-index: 34"
        x-large
        rounded
        color="#2B85C5"
        class="white--text text-capitalize"
        ><v-icon left>mdi-google-play</v-icon>Google Play</v-btn
      >
      <img class="shapes" src="../assets/shapes.svg" alt="shapes" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
.header-container {
  height: 120vh;
  width: 100%;
  display: grid;
  grid-template-columns: auto auto;
  justify-content: space-around;
  align-content: center;
  align-items: center;
  background-image: linear-gradient(90deg, #19d3dc, #18e7d3, #18e7d3, #19d2dd);
  position: relative;
  top: 35px;
}

.shapes {
  position: absolute;
  left: 0;
  margin-top: auto;
  margin-bottom: auto;
  top: 0;
  bottom: 0;
  height: 40%;
}

.header-picture {
  z-index: 5;
}

.h1-style {
  font-size: 5rem;
  line-height: 1;
}

.p-style {
  font-size: 1.5rem;
}

@media (max-width: 1000px) {
  .header-picture {
    display: none;
  }
}

@media (max-width: 500px) {
  .h1-style {
    font-size: 40px;
  }
  .p-style {
    font-size: 20px;
  }

  .shapes {
    height: 20%;
  }
}

@media (max-width: 550px) {
  .shapes {
    height: 20%;
  }
}
</style>
