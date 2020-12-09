<template>
  <div class="container" id="guide">
    <div>
      <h1 class="text-uppercase display-1 font-weight-bold ma-5" style="color: #19d3cc">
        Qo'llanma
      </h1>
    </div>
    <v-item-group>
      <v-container>
        <v-row>
          <v-col v-for="instruction in Instructions" :key="instruction" cols="12" md="4">
            <div class="instruction-cards">
              <div class="rounded-cards">
                <img src="../assets/image6.png" alt="" />
              </div>
            </div>
            <div class="instruction-txt">
              <div>
                {{ instruction }}
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-item-group>
  </div>
</template>

<script>
export default {
  name: "Instructions",

  data() {
    return {
      Instructions: [
        "1. Muammoni suratga oling!",
        "2. Rasmga olingan fotoga izoh qoldiring.",
        "3. Natijalarni kuzatib boring",
      ],
    };
  },
};
</script>
<style>
.title {
  font-family: Open Sans;
  font-style: normal;
  font-weight: bold;
  font-size: 22px;
  color: #19d3cc;
  position: relative;
  text-transform: uppercase;
  margin-bottom: 35px;
}
.title::before {
  position: absolute;
  left: 0;
  top: 1.5em;
  height: 0;
  width: 50px;
  content: "";
  border: 1px solid #19d3cc;
}
.rounded-cards {
  width: 327px;
  height: 327px;
  border-radius: 100% !important;
  background: #19d3cc;
  display: flex;
  align-items: center;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  margin: 0 auto;
}
.rounded-cards img {
  height: 233px;
  margin: 0 auto;
}
.instruction-txt {
  font-weight: bold;
  font-size: 20px;
  line-height: 27px;
  color: #696969;
  text-align: center;
  margin-top: 40px;
}
@media (max-width: 1265px) {
  .rounded-cards {
    width: 227px;
    height: 227px;
  }
  .rounded-cards img {
    height: 133px;
  }
}
</style>
