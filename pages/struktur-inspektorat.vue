<template>
    <div class="struktur_inspektorat-container">
        <!-- <Navbar/> -->
        <Team/>
        <Footer/>
    </div>
</template>

<script>
import Team from "~/components/organisms/Team"
import Footer from "~/components/organisms/Footer"
import Navbar from '~/components/organisms/Navbar.vue'
export default {
    components: {
        Team,
        Footer,
        Navbar,
    }

}
</script>

<style>

</style>