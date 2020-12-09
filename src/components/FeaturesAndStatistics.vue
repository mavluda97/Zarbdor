<template>
  <div class="outer-container" id="features">
    <div class="common-container mb-16">
      <div class="up-container pa-5 pb-16">
        <h1 class="text-uppercase display-1 font-weight-bold ma-10 white--text">
          Afzalliklar
        </h1>
        <div class="feature-container ma-10">
          <div
            v-for="value in Features"
            :key="value.index"
            class="feature-lists"
          >
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
        one: [
          "Muammoning tezkor yechimi",
          "Ushbu ilova orqali fuqarolar o'z murojaatlarini tez va oson yo'llaydilar. Qisqa muddat ichida muammolar hal qilinadi",
          "mdi-laptop-mac",
        ],
        two: [
          "Mutasaddi tashkilotlar bilan to'g'ridan to'g'ri muloqot",
          "Fuqarolarning murojaatlari to'g'ridan to'g'ri mutassadi tashkilotlarga yuboriladi va ular zudlik bilan mazkur muammolar yechimi bilan shug'ullanadilar. ",
          "mdi-laptop-mac",
        ],
        three: [
          "Muammolar yechilishi ustidan online nazorat",
          "Fuqarolar nafaqat o'z murojatlarini yuborishi, balki endilikda ular ham muammolarning hal bo'lish jarayonini online nazorat qila olashi mumkin",
          "mdi-laptop-mac",
        ],
        four: [
          "Murojaatlarni yetqazish uchun qulay tizim",
          "Ushbu ilova orqali murojaatlarning yuborilishi juda qulay bo'lganligi uchun fuqarolar endi hech qanday navbat kutmaydilar, ortiqcha ovoragarchiliklar ularni be'zovta qilmaydi.",
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
  height: 900px;
}

@media (min-width: 671px) and (max-width: 680px) {
  .outer-container {
    height: 850px;
  }
}

@media (min-width: 636px) and (max-width: 670px) {
  .outer-container {
    height: 900px;
  }
}

@media (min-width: 542px) and (max-width: 635px) {
  .outer-container {
    height: 1000px;
  }
}

@media (min-width: 501px) and (max-width: 541px) {
  .outer-container {
    height: 1100px;
  }
}

@media (min-width: 409px) and (max-width: 500px) {
  .outer-container {
    height: 1600px;
  }
}

@media (min-width: 377px) and (max-width: 408px) {
  .outer-container {
    height: 1800px;
  }
}

@media (min-width: 345px) and (max-width: 376px) {
  .outer-container {
    height: 1900px;
  }
}

@media (min-width: 302px) and (max-width: 344px) {
  .outer-container {
    height: 2100px;
  }
}

@media (max-width: 301px) {
  .outer-container {
    height: 2400px;
  }
}

@media (max-width: 285px) {
  .outer-container {
    height: 2500px;
  }
}
</style>
