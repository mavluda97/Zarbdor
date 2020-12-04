<template>
  <v-app>
    <!--Mavluda part -->
    <Navbar/>
    <Header/>
    <About/>
    <FeaturesAndStatistics/>

    <!--Anora part -->
    <Services/>
    <Instructions/>
    <Results/>
    <Footer/>

  </v-app>
</template>

<script>

// Mavluda part
import Navbar from "./components/Navbar";
import Header from "./components/Header";
import About from "./components/About";
import FeaturesAndStatistics from "./components/FeaturesAndStatistics";

// Anora part
import Services from "./components/Services";
import Instructions from "./components/Instructions";
import Results from "./components/Results";
import Footer from "./components/Footer";


export default {
  name: "App",

  components: {
    Navbar,
    Header,
    About,
    FeaturesAndStatistics,
    Services,
    Instructions,
    Results,
    Footer
  },

  data (){
    //
  } 
};
</script>
