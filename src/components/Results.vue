<template>
    <div class="container">
        <div class="title"
        left>
            Natija
        </div>
         <div class="results-block">
            <div class="images" >
                <v-carousel
                    height="100%"
                    
                    hide-delimiter-background
                    show-arrows
                    cycle
                    pa-10
                    >
                    <v-carousel-item class="slider-content"
                    >
                    <div  class="slider-photos" >     
                        <div class="results-txt">
                            <div class="res-title">Muammo</div>
                            <p> Ko'cha muzlab qolgan, yurishga qiynalyabmiz. Iltimos muzlardan tozalashga yordam bering  </p>
                        </div>
                         <div class="ba-image">
                            <div class="sticker">Before</div>
                         <img
                            src="../assets/problem.png"
                            height="100%"
                            width="auto">
                        </div> 
                    </div>
                           
                    <div  class="slider-photos">
                         <div class="results-txt">
                            <div class="res-title">Yechim</div>
                            <p> - Мирзо Улугбек туман Ободонлаштириш бошкармаси томонидан Мустакиллик шох кучасидаги пиёдалар йулаги музландан тозаланди  </p>
                        </div>
                   <div class="ba-image">
                            <div class="sticker">After</div>
                         <img
                            src="../assets/problem.png"
                            height="100%"
                            width="auto">
                        </div> 
                    </div>
                  
                    </v-carousel-item>      
                      <v-carousel-item class="slider-content"
                    >
                    <div  class="slider-photos" >     
                        <div class="results-txt">
                            <div class="res-title">Muammo</div>
                            <p> Ko'cha muzlab qolgan, yurishga qiynalyabmiz. Iltimos muzlardan tozalashga yordam bering  </p>
                        </div>
                         <div class="ba-image">
                            <div class="sticker">Before</div>
                         <img
                            src="../assets/problem.png"
                            height="100%"
                            width="auto">
                        </div> 
                    </div>
                           
                    <div  class="slider-photos">
                         <div class="results-txt">
                            <div class="res-title">Yechim</div>
                            <p> - Мирзо Улугбек туман Ободонлаштириш бошкармаси томонидан Мустакиллик шох кучасидаги пиёдалар йулаги музландан тозаланди  </p>
                        </div>
                   <div class="ba-image">
                            <div class="sticker">After</div>
                         <img
                            src="../assets/problem.png"
                            height="100%"
                            width="auto">
                        </div> 
                    </div>
                  
                    </v-carousel-item>   
                      <v-carousel-item class="slider-content"
                    >
                    <div  class="slider-photos" >     
                        <div class="results-txt">
                            <div class="res-title">Muammo</div>
                            <p> Ko'cha muzlab qolgan, yurishga qiynalyabmiz. Iltimos muzlardan tozalashga yordam bering  </p>
                        </div>
                         <div class="ba-image">
                            <div class="sticker">Before</div>
                         <img
                            src="../assets/problem.png"
                            height="100%"
                            width="auto">
                        </div> 
                    </div>
                           
                    <div  class="slider-photos">
                         <div class="results-txt">
                            <div class="res-title">Yechim</div>
                            <p> - Мирзо Улугбек туман Ободонлаштириш бошкармаси томонидан Мустакиллик шох кучасидаги пиёдалар йулаги музландан тозаланди  </p>
                        </div>
                   <div class="ba-image">
                            <div class="sticker">After</div>
                         <img
                            src="../assets/problem.png"
                            height="100%"
                            width="auto">
                        </div> 
                    </div>
                  
                    </v-carousel-item>   
                      <v-carousel-item class="slider-content"
                    >
                    <div  class="slider-photos" >     
                        <div class="results-txt">
                            <div class="res-title">Muammo</div>
                            <p> Ko'cha muzlab qolgan, yurishga qiynalyabmiz. Iltimos muzlardan tozalashga yordam bering  </p>
                        </div>
                         <div class="ba-image">
                            <div class="sticker">Before</div>
                         <img
                            src="../assets/problem.png"
                            height="100%"
                            width="auto">
                        </div> 
                    </div>
                           
                    <div  class="slider-photos">
                         <div class="results-txt">
                            <div class="res-title">Yechim</div>
                            <p> - Мирзо Улугбек туман Ободонлаштириш бошкармаси томонидан Мустакиллик шох кучасидаги пиёдалар йулаги музландан тозаланди  </p>
                        </div>
                   <div class="ba-image">
                            <div class="sticker">After</div>
                         <img
                            src="../assets/problem.png"
                            height="100%"
                            width="auto">
                        </div> 
                    </div>
                  
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
    padding: auto;
}
.images{
    min-width: 100%;
    margin: 0 auto;
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
.slider-photos{
    display: flex;
    justify-content: space-between;
}
.ba-image{
    width: 350px;
    height: 300px;
    position: relative;
    margin: 0 auto;
    margin-bottom: 10px;
}
.sticker{
    width: 100px;
    height: 40px;
    background-color: #19D3CC;
    font-size: 20px;
    color: white;
    position: absolute;
    right: 0px;
    padding-top: 2%;
    text-align: center;

}
.slider-content{
    padding: 10%;
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
    min-width: 100%;
}
.results-txt p{
    font-size: 14px;
}
.ba-image{
    width: 250px;
    height: 200px;
    position: relative;
    margin-bottom: 10px;
}

.v-window__prev, .v-window__next{
    margin: 0;
}
.sticker{
    right: 15px;
}
}
@media (max-width: 700px){
    .results-block{
        margin: 5px;
    }
.images{
    min-width: 100%;
}
.slider-content{
    padding: 7% 15%;
}
.slider-photos{
    flex-direction: column;
}
.v-window__prev, .v-window__next{
    margin: 0;
}
.v-btn--icon.v-size--default {
    height: 25px;
    width: 25px;
}
.sticker{
    right: 18px;
}
}

@media (max-width: 400px){
       .results-block{
        margin: 5px;
    }
.images{
    min-width: 100%;
}
.slider-content{
    padding: 0 15%;
}
.v-window__prev, .v-window__next{
    margin: 0;
}
.v-btn--icon.v-size--default {
    height: 25px;
    width: 25px;
}
.sticker{
    right: 18px;
}
}
</style>