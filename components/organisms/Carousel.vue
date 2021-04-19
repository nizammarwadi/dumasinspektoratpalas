<template>
    <div id="slider" class="slider">
        <div id="carouselExampleCaptions" class="carousel slide" data-ride="carousel">
            <ol class="carousel-indicators">
                <li data-target="#carouselExampleCaptions" data-slide-to="0" class="active"></li>
                <li data-target="#carouselExampleCaptions" data-slide-to="1"></li>
                <li data-target="#carouselExampleCaptions" data-slide-to="2"></li>
            </ol>
            <div class="carousel-inner ">
                <div class="carousel-item active">
                <img src="~/assets/images/kantor.jpg" class="d-block w-100" alt="#">
                <div class="carousel-caption d-sm-block ">
                    <h1 class="display-none">SELAMAT DATANG DI WEBSITE KAMI</h1>
                    <p class="lead">Pusat Pelayanan Informasi Masyarakat Desa Siundol Dolok</p>
                    <ButtonElement
                        titleBtn="HUBUNGI"
                    />
                </div>
                </div>
                <div class="carousel-item">
                <img src="~/assets/images/dpr.jpg" class="d-block w-100" alt="#">
                <div class="carousel-caption d-sm-block">
                    <h1 class="display-none">SELAMAT DATANG DI WEBSITE KAMI</h1>
                    <p class="lead">Pusat Pelayanan Informasi Masyarakat Desa Siundol Dolok</p>
                </div>
                </div>
                <div class="carousel-item">
                <img src="~/assets/images/dpr.jpg" class="d-block w-100" alt="#">
                <div class="carousel-caption d-sm-block">
                    <h1 class="display-none">SELAMAT DATANG DI WEBSITE KAMI</h1>
                    <p class="lead">Pusat Pelayanan Informasi Masyarakat Desa Siundol Dolok</p>
                </div>
                </div>
            </div>
            <a class="carousel-control-prev" href="#carouselExampleCaptions" role="button" data-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="sr-only">Previous</span>
            </a>
            <a class="carousel-control-next" href="#carouselExampleCaptions" role="button" data-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="sr-only">Next</span>
            </a>
        </div>
    </div>
   
</template>

<script>
import Button from '~/components/atoms/Button.vue'
export default {
    components: {
        ButtonElement: Button,
    }
}
</script>

<style>
    .slider {
        width: 100%;
    }
    .carousel-inner {
        margin-top: 70px;
    }
    .carousel-item img {
        height: 550px;
    }
    .carousel-caption h1 {
        font-weight: bold;
        font-size: 37px;
    }
    .carousel-caption p {
        font-size: 18px;
    }
    @media only screen and (max-width: 680px) {
        .slider h1{
            width: 100%;
            font-size: 20px;
            font-weight: bold;
        }
        .slider p {
            font-size: 15px;
        }
        .lead{
            font-size: 14px;
        }
        .carousel-item img{
            width: 100%;
            height: 350px;
        }
   } 
</style>