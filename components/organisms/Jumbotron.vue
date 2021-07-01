<template>
    <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
  <ol class="carousel-indicators">
    <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
  </ol>
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img class="d-block w-100" src="~/assets/images/indonesiaku.png" alt="First slide">
            <div class="carousel-caption d-md-block">
                <h1 class="display-4">Elektronik <span>Pengaduan</span> Masyarakat Inspektorat  <span>Padang Lawas</span></h1>
                <p><button class="btn btn-primary btn-lg mt-4" @click="toRegistrasiSection">LAPOR SEKARANG</button></p>
            </div>
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="~/assets/images/depan kantor.png" alt="Second slide">
            <div class="carousel-caption d-md-block">
                <h1 class="display-4">Elektronik <span>Pengaduan</span> Masyarakat Inspektorat  <span>Padang Lawas</span></h1>
                <p><button class="btn btn-primary btn-lg mt-4" @click="toRegistrasiSection">LAPOR SEKARANG</button></p>
            </div>
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="~/assets/images/laptop.jpg" alt="Third slide">
            <div class="carousel-caption d-md-block">
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
</div>
</template>

<script>
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
        height: 36rem;
        margin-top: 0px;
    }
    .carousel-caption {
        margin-bottom: 60px;
    }
   
    /* .jumbotron::after {
        content: '';
        display: block;
        width: 100%;
        height: 100%;
        background-image: linear-gradient(to top, rgba(0,0,0,0), rgba(0,0,0,0.0));
        position: absolute;
        bottom: 0;
        
    } */
    /* .jumbotron .container {
        z-index: 1;
        position: relative;
    } */
    /* .carousel-caption .display-4 {
        color: white;
        text-align: center;
        margin-top: 15rem;
        text-shadow: 1px px 1px rgb(0, 0, 0, 0.7);
        font-size: 50px;
    } */
    @media (max-width: 792px) {
        .carousel-item {
            height: 28rem;
        }
        .carousel-item img {
            height: 400px;
        }
         .carousel-caption .display-4 {
            color: white;
            text-align: center;
            margin: 12rem auto 0px;
            text-shadow: 1px px 1px rgb(0, 0, 0, 0.7);
            font-size: 25px;
         }
         .btn {
            padding: 5px 10px;
            font-size: 17px;
         }
    }
     @media (max-width: 422px) {
         .carousel-caption .display-4 {
            color: white;
            text-align: center;
            margin: 10rem auto 0px;
            text-shadow: 1px px 1px rgb(0, 0, 0, 0.7);
            font-size: 20px;
         }
         .btn {
            padding: 3px 7px;
            font-size: 16px;
         }
     }
</style>