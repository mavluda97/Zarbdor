<template>
  <div class="container" id="guide">
    <div>
      <h1 class="text-uppercase headline font-weight-bold " style="color: #19d3cc">
        {{$t('Qollanma')}}
      </h1>
    </div>
    <v-item-group>
      <v-container>
        <v-row>
          <v-col v-for="i in Instructions" :key="i" cols="12" md="4">
            <div class="instruction-cards">
              <div class="rounded-cards">
                <img :src="require(`@/assets/${i.img}`)" alt="pic" />
              </div>
            </div>
            <div class="instruction-txt">
              <div>
                {{ $t(i.name) }}
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
        {
          img: "pic1.png",
          name: "guide-1",
        },
        {
          img: "pic2.png",
          name: "guide-2",
        },
        {
          img: "pic3.png",
          name: "guide-3",
        },
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
  height: 300px;
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
    height: 215px;
  }
}
</style>
