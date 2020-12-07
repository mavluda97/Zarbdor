<template >
    <div class="container" >
           <div class="title">
       Xizmat turlari
        </div>
        <v-sheet
            class="mx-auto"
            max-width="100%"
            height="auto"
            >
         
            <v-slide-group
                show-arrows
                height="205"
                center-active
                v-model="model"
            >
                <v-slide-item
                v-for="n in Services"
                :key="n"
                centered
                pt-5
                >
                <v-card width="190"                
                height="175"
                class="mx-2 card-content"
                centered>
                    <v-img
                    src="../assets/services.png"
                    height="auto"
                    width="71"
                    pt-15
                    style="margin: 0 auto"></v-img>
                    <div class="service-name" centered>{{n}}</div>
                </v-card>
              
                </v-slide-item>
            </v-slide-group>
        </v-sheet>
    </div>
</template>

<script>
export default {
    name: 'Services',
      data () {
    return {
      Services: [
          'Soliq hizmati', 'KADASTR MUAMMOSi', 'GARAJ MUAMMOSI', 'Ko’chalarni yoritish', 'Aloqa Tarmog’i', 'SANITARIYA VA GIGIYENA', 'GARAJ MUAMMOSI', 'Ko’chalarni yoritish', 'Aloqa Tarmog’i', 'SANITARIYA VA GIGIYENA'
      ],
    }
  },
}

</script>

<style scoped>
.container{
    width: 100%;
    margin-bottom: 80px;
}
.service-name{
    font-family: Open Sans;
font-style: normal;
font-weight: 600;
font-size: 14px;
line-height: 19px;
/* identical to box height */
text-align: center;
padding-top: 20px;
text-transform: uppercase;
color: #6E6E6E;
}
.v-item-group{
    height: 195px;
}
.card-content{
    padding-top: 29px;
    margin: 3px auto;
    border-radius: 8px;
}
.v-slide-group__wrapper{
    margin-top: 5px;
}
@media (max-width:1265px) {
.mx-auto{
    max-width: 100%;
}

}
</style>