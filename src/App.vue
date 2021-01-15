<template>
  <v-app style="background-color: #e5e5e5">
    <!--Mavluda part -->
    <Preloader />
    <Navbar />
    <Header />
    <About />
    <FeaturesAndStatistics />

    <!--Anora part -->
    <Services />
    <Instructions />
    <Results />
    <Footer />
  </v-app>
</template>

<script>
window.replainSettings = { id: '0d714563-bb94-4f5e-8420-e7f7a12fdcbe' };
(function(u){var s=document.createElement('script');s.type='text/javascript';s.async=true;s.src=u;
var x=document.getElementsByTagName('script')[0];x.parentNode.insertBefore(s,x);
})('https://widget.replain.cc/dist/client.js');

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
import Preloader from "./components/PageLoader";

export default {
  name: "App",

  components: {
    Preloader,
    Navbar,
    Header,
    About,
    FeaturesAndStatistics,
    Services,
    Instructions,
    Results,
    Footer,
  },
  
  created(){
        document.title = "Obod-Zarbdor"
  },

  data() {
    return {};
  },
};
</script>


