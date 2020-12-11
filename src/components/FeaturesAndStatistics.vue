<template>
  <div id="features">
    <div class="common-container mb-16">
      <div class="up-container pa-5 pb-16">
        <h1 class="text-uppercase headline font-weight-bold ma-10 white--text">
          {{ $t("Afzalliklar") }}
        </h1>
        <div class="feature-container ma-10">
          <div v-for="value in Features" :key="value.index" class="feature-lists">
            <v-icon class="ma-5 white--text features-icons" x-large>{{
              value[2]
            }}</v-icon>
            <h3 class="mx-5 white--text font-weight-bold">
              {{ $t(value[0]) }}
            </h3>
            <p class="ma-5 white--text">
              {{ $t(value[1]) }}
            </p>
          </div>
        </div>
      </div>
      <div class="down-container pa-5">
        <div v-for="(value, name) in datas" :key="name.index">
          <p class="display-2 white--text text-center">{{ value }}</p>
          <p class="white--text text-center font-weight-light">
            {{ $t(name) }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Categories from "../services/Categories";
export default {
  name: "FeaturesAndStatistics",

  data() {
    return {
      base: process.env.VUE_APP_BASE_URL,
      Features: {
        one: ["birinchi-afzal", "bir-afzal-def", "mdi-laptop-mac"],
        two: ["ikkinchi-afzal", "ikki-afzal-def", "mdi-laptop-mac"],
        three: ["uchinchi-afzal", "uch-afzal-def", "mdi-laptop-mac"],
        four: ["tortinchi-afzal", "tort-afzal-def", "mdi-laptop-mac"],
      },

      datas: {
        Problems: 0,
        Viewed: 0,
        Solved: 0,
        Rejected: 0,
        Average: 0,
      },
    };
  },

  methods: {
    getReports() {
      Categories.getStats()
        .then((res) => {
          this.datas.Problems = res.data.all;
          this.datas.Viewed = res.data.reviewed;
          this.datas.Solved = res.data.closed;
          this.datas.Rejected = res.data.rejected;
        })
        .catch((err) => {
          console.log(err);
        });
    },
    getTime() {
      Categories.getTime().then((res) => {
        this.datas.Average = res.data.avgTime;
      });
    },
  },
  created() {
    this.getReports();
    this.getTime();
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
  grid-template-rows: 410px;
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
  height: 160px;
  width: 100%;
  display: grid;
  grid-template-columns: auto auto auto auto auto;
  column-gap: 20px;
  justify-content: space-evenly;
  align-content: center;
  text-align: center;
  background-color: #3d3d3d;
  padding-right: 15px;
  padding-left: 15px;
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

@media (max-width: 715px) {
  .down-container {
    height: 550px;
    grid-template-columns: auto;
  }
}
</style>
