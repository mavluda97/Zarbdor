<template>
    <div class="container">
        <div class="title"
        left>
            Natija
        </div>
         <div class="results-block">
            <div class="mobile-res">
                <div class="results-txt">
                <div class="res-title">Muammo</div>
                <p> Ko'cha muzlab qolgan, yurishga qiynalyabmiz. Iltimos muzlardan tozalashga yordam bering  </p>
                </div>
                <div style="" class="line"></div>
                <div class="results-txt">
                    <div class="res-title">Yechim</div>
                    <p> - Мирзо Улугбек туман Ободонлаштириш бошкармаси томонидан Мустакиллик шох кучасидаги пиёдалар йулаги музландан тозаланди  </p>
                </div>
            </div>
            <div class="images" >
                <v-carousel
                    height="400"
                    hide-delimiter-background
                    show-arrows
                    >
                        <v-carousel-item class="d-flex"
                    >
                    <img
                    src="../assets/problem.png"
                    height="300"
                    width="300">
                     <img
                    src="../assets/result.png"
                    height="300"
                    width="300">
                    </v-carousel-item>
                    
                        <v-carousel-item class="d-flex"
                    >
                    <img
                    src="../assets/image6.png"
                    height="400"
                    width="auto">
                     <img
                    src="../assets/image7.png"
                    height="400"
                    width="auto">
                    </v-carousel-item>
                    
                </v-carousel>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Results',
      data () {
    return {
      colors: [
        'indigo',
        'warning',
        'pink darken-2',
        'red lighten-1',
        'deep-purple accent-4',
      ],
      slides: [
        'First',
        'Second',
        'Third',
        'Fourth',
        'Fifth',
      ],
    }
  },
}

</script>

<style scoped>
.results-block{
    margin-left: 5%;
    display: flex;
    justify-content: space-between;
}
.results-txt .res-title{
   font-family: Open Sans;
    font-style: normal;
    font-weight: bold;
    font-size: 20px;
    line-height: 27px;
    color: #696969;
    margin-bottom: 16px;
}
.results-txt p{
    font-weight: normal;
    font-size: 18px;
    line-height: 25px;
    color: #696969;
    max-width: 300px;
}
.images{
    min-width: 600px;
}
.line{
    border: 1px solid #CCCCCC; 
    margin: 32px auto; 
    width:300px
}
.before-after{
    display: flex;
    justify-content: space-between;
}
@media (max-width: 1265px){
.mobile-res{
    display: flex;
    justify-content: space-between;
}
.line{
    display: none;
}
.results-block{
    flex-direction: column;
    margin: 5%;
}
.images{
    min-width: 300px;
}
.results-txt p{
    font-size: 14px;
    max-width: 250px;
}
}
</style>