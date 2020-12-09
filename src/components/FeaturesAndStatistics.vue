<template>
  <div class="outer-container" id="features">
    <div class="common-container mb-16">
      <div class="up-container pa-5 pb-16">
        <h1 class="text-uppercase display-1 font-weight-bold ma-10 white--text">
          Afzalliklar
        </h1>
        <div class="feature-container ma-10">
          <div v-for="value in Features" :key="value.index" class="feature-lists">
            <v-icon class="ma-5 white--text features-icons" x-large>{{
              value[2]
            }}</v-icon>
            <h3 class="mx-5 white--text font-weight-bold">
              {{ value[0] }}
            </h3>
            <p class="ma-5 white--text">
              {{ value[1] }}
            </p>
          </div>
        </div>
      </div>
      <div class="down-container pa-5">
        <div v-for="(value, name) in datas" :key="name.index">
          <p class="display-2 white--text text-center">{{ value }}</p>
          <p class="white--text text-center font-weight-light">{{ name }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FeaturesAndStatistics",

  data() {
    return {
      Features: {
        one: [
          "Muammoning tezkor yechimi",
          "Muammoni suratga oling! Tizim orqali sizning sorovingiz qabul qilingani yoki ishlash jarayonida ekanligi togrisida nazorat o'rnating",
          "mdi-laptop-mac",
        ],
        two: [
          "Mutasaddi tashkilotlar bilan to'g'ridan to'g'ri muloqot",
          "Muammoni suratga oling! Tizim orqali sizning sorovingiz qabul qilingani yoki ishlash jarayonida ekanligi togrisida nazorat o'rnating",
          "mdi-laptop-mac",
        ],
        three: [
          "Muammolar yechilishi ustidan online nazorat",
          "Muammoni suratga oling! Tizim orqali sizning sorovingiz qabul qilingani yoki ishlash jarayonida ekanligi togrisida nazorat o'rnating",
          "mdi-laptop-mac",
        ],
        four: [
          "Murojaatlarni yetqazish uchun qulay tizim",
          "Muammoni suratga oling! Tizim orqali sizning sorovingiz qabul qilingani yoki ishlash jarayonida ekanligi togrisida nazorat o'rnating",
          "mdi-laptop-mac",
        ],
      },

      datas: {
        Problems: 76,
        Viewed: 3,
        Solved: 43,
        Rejected: 16,
        Average: 14,
      },
    };
  },
};
</script>

<style scoped>
.common-container {
  background-color: #e5e5e5;
  width: 100%;
  position: relative;
}

.up-container {
  background-image: linear-gradient(90deg, #19d3dc, #18e7d3, #18e7d3, #19d2dd);
  width: 100%;
}

.feature-container {
  display: grid;
  grid-template-columns: auto auto auto auto;
  grid-template-rows: 400px;
  column-gap: 20px;
}

.feature-lists {
  border: 2px solid #fff;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.down-container {
  border: 2px solid #3d3d3d;
  border-radius: 20px;
  height: 160px;
  width: 800px;
  display: grid;
  grid-template-columns: auto auto auto auto auto;
  justify-content: space-around;
  align-content: center;
  position: absolute;
  top: 93%;
  margin-left: auto;
  margin-right: auto;
  left: 0;
  right: 0;
  text-align: center;
  background-color: #3d3d3d;
}

@media (max-width: 1100px) {
  .feature-container {
    grid-template-columns: auto auto;
    grid-template-rows: auto auto;
    row-gap: 20px;
  }
}

@media (min-width: 671px) and (max-width: 980px) {
  .features-icons {
    display: none;
  }
}

@media (max-width: 670px) {
  .feature-container {
    grid-template-columns: auto;
    grid-template-rows: auto auto auto auto;
    row-gap: 20px;
  }

  .features-icons {
    display: none;
  }
}

@media (min-width: 501px) and (max-width: 850px) {
  .down-container {
    width: 500px;
  }
}

@media (max-width: 500px) {
  .down-container {
    width: 100%;
    height: 600px;
    grid-template-columns: auto;
  }
}

.outer-container {
  height: 800px;
}

@media (min-width: 671px) and (max-width: 680px) {
  .outer-container {
    height: 800px;
  }
}

@media (min-width: 636px) and (max-width: 670px) {
  .outer-container {
    height: 850px;
  }
}

@media (min-width: 501px) and (max-width: 635px) {
  .outer-container {
    height: 1000px;
  }
}

@media (min-width: 408px) and (max-width: 500px) {
  .outer-container {
    height: 1600px;
  }
}

@media (min-width: 360px) and (max-width: 407px) {
  .outer-container {
    height: 1800px;
  }
}

@media (min-width: 305px) and (max-width: 359px) {
  .outer-container {
    height: 2000px;
  }
}

@media (max-width: 304px) {
  .outer-container {
    height: 2200px;
  }
}
</style>
