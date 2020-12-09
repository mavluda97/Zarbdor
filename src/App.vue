<template>
  <v-app style="background-color: #e5e5e5">
    <!--Mavluda part -->
    <Preloader />
    <Navbar/>
    <Header/>
    <About/>
    <FeaturesAndStatistics/>
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
import Preloader from './components/PageLoader';

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

  data() {
    //
  },
};
</script>


