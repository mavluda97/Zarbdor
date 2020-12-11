<template>
  <div v-if="slides.length > 0" class="container">
    <div>
      <h1 class="text-uppercase headline font-weight-bold ma-5" style="color: #19d3cc">
        {{ $t("Natija") }}
      </h1>
    </div>
    <div class="results-block">
      <div class="images">
        <v-carousel height="100%" hide-delimiter-background show-arrows cycle pa-10>
          <v-carousel-item v-for="slide in slides" :key="slide.id" class="slider-content">
            <div class="slider-photos">
              <div class="results-txt">
                <div class="res-title">{{ $t("Muammo") }}</div>
                <p>
                  {{ slide.comments[0].text }}
                </p>
              </div>
              <div class="ba-image">
                <div class="sticker">{{ $t("Muammo") }}</div>
                <v-img
                  :src="slide.comments[0].image.imageUrl"
                  :lazy-src="base_url + slide.comments[0].image.imageUrl"
                  height="100%"
                  width="auto"
                  :alt="slide.comments[0].image.imageUrl"
                />
              </div>
            </div>

            <div class="slider-photos">
              <div class="results-txt">
                <div class="res-title">{{ $t("Yechim") }}</div>
                <p>
                  {{ slide.comments[1].text }}
                </p>
              </div>
              <div class="ba-image">
                <div class="sticker">{{ $t("Yechim") }}</div>
                <v-img
                  :src="base_url + slide.comments[1].image.imageUrl"
                  :lazy-src="base_url + slide.comments[1].image.imageUrl"
                  height="100%"
                  width="auto"
                  :alt="slide.comments[1].image.imageUrl"
                />
              </div>
            </div>
          </v-carousel-item>
        </v-carousel>
      </div>
    </div>
  </div>
</template>

<script>
import Categories from "../services/Categories";

export default {
  name: "Results",
  data() {
    return {
      base: process.env.VUE_APP_BASE_URL,
      base_url: process.env.VUE_APP_VARIABLE,

      colors: [
        "indigo",
        "warning",
        "pink darken-2",
        "red lighten-1",
        "deep-purple accent-4",
      ],
      slides: [],
      // slides: ["First", "Second", "Third", "Fourth", "Fifth"]
    };
  },
  methods: {
    getResults() {
      Categories.getResults()
        .then((res) => {
          this.slides = res.data;
        })
        .catch((err) => {
          console.log(err);
        });
    },
  },
  created() {
    this.getResults();
  },
};
</script>

<style scoped>
.results-block {
  margin-left: 5%;
  display: flex;
  justify-content: space-between;
}
.results-txt .res-title {
  font-family: Open Sans;
  font-style: normal;
  font-weight: bold;
  font-size: 20px;
  line-height: 27px;
  color: #696969;
  margin-bottom: 16px;
}
.results-txt p {
  font-weight: normal;
  font-size: 18px;
  line-height: 25px;
  color: #696969;
  max-width: 300px;
  padding: auto;
}
.images {
  min-width: 100%;
  margin: 0 auto;
}
.line {
  border: 1px solid #cccccc;
  margin: 32px auto;
  width: 300px;
}
.before-after {
  display: flex;
  justify-content: space-between;
}
.slider-photos {
  display: flex;
  justify-content: space-between;
  width: 80%;
  margin: 0 auto;
}
.ba-image {
  width: 350px;
  height: 300px;
  position: relative;
  margin-bottom: 10px;
  z-index: 444;
}
.sticker {
  width: 100px;
  height: 40px;
  background-color: #19d3cc;
  font-size: 20px;
  color: white;
  position: absolute;
  right: 0px;
  padding-top: 2%;
  text-align: center;
}
.slider-content {
  padding: 10%;
}
@media (max-width: 1265px) {
  .mobile-res {
    display: flex;
    justify-content: space-between;
  }
  .line {
    display: none;
  }
  .results-block {
    flex-direction: column;
    margin: 5%;
  }
  .images {
    min-width: 100%;
  }
  .results-txt p {
    font-size: 14px;
  }
  .ba-image {
    width: 250px;
    height: 200px;
    position: relative;
    margin-bottom: 10px;

  }

  .v-window__prev,
  .v-window__next {
    margin: 0;
  }
  .sticker {
    right: 15px;
  }
}
@media (max-width: 700px) {
  .results-block {
    margin: 5px;
  }
  .images {
    min-width: 100%;
  }
  .slider-content {
    padding: 7% 15%;
  }
  .slider-photos {
    flex-direction: column;
  }
  .v-window__prev,
  .v-window__next {
    margin: 0;
  }
  .v-btn--icon.v-size--default {
    height: 25px;
    width: 25px;
  }
  .sticker {
    right: 18px;
  }
}

@media (max-width: 400px) {
  .results-block {
    margin: 5px;
  }
  .images {
    min-width: 100%;
  }
  .slider-content {
    padding: 0 15%;
  }
  .v-window__prev,
  .v-window__next {
    margin: 0;
  }
  .v-btn--icon.v-size--default {
    height: 25px;
    width: 25px;
  }
  .sticker {
    right: 18px;
  }
}
</style>
