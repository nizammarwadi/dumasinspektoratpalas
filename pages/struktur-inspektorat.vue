<template>
    <div class="struktur-inspektorat-container">
        <NavbarNew/>
        <Team/>
        <Footer/>
    </div>
</template>

<script>
import NavbarNew from "~/components/organisms/NavbarNew"
import Team from "~/components/organisms/Team"
import Footer from "~/components/organisms/Footer"
export default {
    components: {
        NavbarNew,
        Team,
        Footer,
    }
}
</script>

<style>

</style>