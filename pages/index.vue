<template>
  <div>
    <Navbar/>
    <PanelTop/>
    <Jumbotron/>
    <Panel/>
    <!-- <Carousel/> -->
    <About/>
    <Principle/>
    <Rules/>
    <Flow/>
    <Counter/>
    <!-- <Team/>/ -->
    <Registrasi/>
    <Footer/>
    <ButtonResponse/>
  </div>
</template>

<script>
import PanelTop from "~/components/organisms/PanelTop"
import Navbar from "~/components/organisms/Navbar"
import Jumbotron from "~/components/organisms/Jumbotron"
import Panel from "~/components/organisms/Panel"
// import Carousel from "~/components/organisms/Carousel"
import About from "~/components/organisms/About"
import Principle from "~/components/organisms/Principle"
import Rules from "~/components/organisms/Rules.vue"
import Flow from "~/components/organisms/Flow"
import Counter from "~/components/organisms/Counter.vue"
import Team from "~/components/organisms/Team"
import Registrasi from "~/components/organisms/Registrasi"
import Footer from "~/components/organisms/Footer"
import ButtonResponse from "~/components/atoms/ButtonResponse"
export default {
  components: {
    Navbar: Navbar,
    PanelTop: PanelTop,
    Jumbotron: Jumbotron,
    Panel: Panel,
    // Carousel: Carousel,
    About: About,
    Principle: Principle,
    Rules: Rules,
    Flow: Flow,
    Counter: Counter,
    Registrasi: Registrasi,
    Team: Team,
    Footer: Footer,
    ButtonResponse,
  }
}
</script>
<style>

</style>