<template>
    <div class="jumbotron jumbotron-fluid">
        <div class="container">
            <h1 class="display-4">Elektronik <span>Pengaduan</span> Masyarakat Inspektorat  <span>Padang Lawas</span></h1>
            <p><button class="btn btn-primary btn-lg mt-4" @click="toRegistrasiSection">LAPOR SEKARANG</button></p>
        </div>
    </div>
</template>

<script>
// import Button from '~/components/atoms/Button.vue'
export default {
    data() {
        return {
            registrasiSection: "",
        }
    },
    mounted() {
        this.registrasiSection = document.getElementById('registrasi')
    },
    methods: {
        toRegistrasiSection() {
            this.registrasiSection.scrollIntoView({
                behavior: "smooth",
                block: "start",
                inline: "nearest"
            })}
        }
    }
</script>

<style>
    .jumbotron{
        background-image: url(~/assets/images/1.jpg);
        /* background-size: contain; */
        background-size: 100% 100%;
        background-position-y: 30px;
        height: 40rem;
        margin-top: 0px;
        position: relative;
    
    }
    .jumbotron::after {
        content: '';
        display: block;
        width: 100%;
        height: 100%;
        background-image: linear-gradient(to top, rgba(0,0,0,1), rgba(0,0,0,0.0));
        /* background-color: blue; */
        /* opacity: .3; */
        position: absolute;
        bottom: 0;
        
    }
    .jumbotron .container {
        z-index: 1;
        position: relative;
    }
    .jumbotron .display-4 {
        color: white;
        /* color: yellow; */
        text-align: center;
        margin-top: 15rem;
        text-shadow: 1px px 1px rgb(0, 0, 0, 0.7);
        font-size: 50px;
    }
    .jumbotron .display-4 span{
        font-weight: 500;
    }.container h1 {
        max-width: 800px;
        margin: 0px auto;
    }
    .container p {
        text-align: center;
    }

</style>