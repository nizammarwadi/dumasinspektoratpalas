<template>
  <div>
    <Navbar/>
    <Jumbotron/>
    <Panel/>
    <!-- <Carousel/> -->
    <About/>
    <Principle/>
    <Flow/>
    <Team/>/
    <Registrasi/>
    <Footer/>
  </div>
</template>

<script>
import Navbar from "~/components/organisms/Navbar"
import Jumbotron from "~/components/organisms/Jumbotron"
import Panel from "~/components/organisms/Panel"
// import Carousel from "~/components/organisms/Carousel"
import About from "~/components/organisms/About"
import Principle from "~/components/organisms/Principle"
import Flow from "~/components/organisms/Flow"
import Team from "~/components/organisms/Team"
import Registrasi from "~/components/organisms/Registrasi"
import Footer from "~/components/organisms/Footer"
export default {
  components: {
    Navbar: Navbar,
    Jumbotron: Jumbotron,
    Panel: Panel,
    // Carousel: Carousel,
    About: About,
    Principle: Principle,
    Flow: Flow,
    Registrasi: Registrasi,
    Team: Team,
    Footer: Footer,
  }
}
</script>

<style>

</style>