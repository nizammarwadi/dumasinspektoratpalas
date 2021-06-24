<template>
    <!-- <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
  <ol class="carousel-indicators">
    <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
  </ol>
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img class="d-block w-100" src="~/assets/images/depan kantor.png" alt="First slide">
            <div class="carousel-caption d-none d-md-block">
                <h1 class="display-4">Elektronik <span>Pengaduan</span> Masyarakat Inspektorat  <span>Padang Lawas</span></h1>
            <p><button class="btn btn-primary btn-lg mt-4" @click="toRegistrasiSection">LAPOR SEKARANG</button></p>
            </div>
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="~/assets/images/depan kantor.png" alt="Second slide">
            <div class="carousel-caption d-none d-md-block">
               <h1 class="display-4">Elektronik <span>Pengaduan</span> Masyarakat Inspektorat  <span>Padang Lawas</span></h1>
            <p><button class="btn btn-primary btn-lg mt-4" @click="toRegistrasiSection">LAPOR SEKARANG</button></p>
            </div>
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="~/assets/images/depan kantor.png" alt="Third slide">
            <div class="carousel-caption d-none d-md-block">
                <h1 class="display-4">Elektronik <span>Pengaduan</span> Masyarakat Inspektorat  <span>Padang Lawas</span></h1>
            <p><button class="btn btn-primary btn-lg mt-4" @click="toRegistrasiSection">LAPOR SEKARANG</button></p>
            </div>
    </div>
  </div>
  <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div> -->
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
    .carousel-item img {
        height: 36.5rem;
        margin-top: 60px;
    }
    .carousel-caption {
        margin-bottom: 100px;
    }
    .jumbotron{
        background-image: url(~/assets/images/1.jpg);
        /* background-size: contain; */
        background-size: 100% 100%;
        background-position-y: 60px;
        height: 40rem;
        margin-top: 0px;
        position: relative;
    
    }
    .jumbotron::after {
        content: '';
        display: block;
        width: 100%;
        height: 100%;
        background-image: linear-gradient(to top, rgba(0,0,0,0), rgba(0,0,0,0.0));
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
    }
    .container h1 {
        max-width: 800px;
        margin: 0px auto;
    }
    .container p {
        text-align: center;
    }
    @media (max-width: 792px) {
         .jumbotron {
             background-size: 100% 100%;
             height: 420px;
             width: 100%;
         }
         .jumbotron .display-4 {
             color: white;
            /* color: yellow; */
            text-align: center;
            width: 400px;
            margin: 12rem auto 0px;
            text-shadow: 1px px 1px rgb(0, 0, 0, 0.7);
            font-size: 25px;
         }
         .btn {
            padding: 5px 10px;
            font-size: 15px;
         }
    }
     @media (max-width: 422px) {
           .jumbotron {
             background-size: 100% 100%;
             height: 350px;
             width: 100%;
         }
         .jumbotron .display-4 {
            width: 320px;
            color: white;
            /* color: yellow; */
            text-align: center;
            margin: 10rem auto 0px;
            text-shadow: 1px px 1px rgb(0, 0, 0, 0.7);
            font-size: 20px;
         }
         .btn {
            padding: 3px 7px;
            font-size: 12px;
         }
     }
</style>