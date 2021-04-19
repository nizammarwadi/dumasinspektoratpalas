<template>
    <footer>
        <section id="footer" class="footer">
            <div class="about-us-title">
                <h5>E-DUMAS INSPEKTORAT PALAS</h5>
            </div>
            <p>E-Dumas Inspektorat Palas adalah Proses Penyampaian Informasi yang berisi keluhan dan ketidakpuasan 
                yang disampaikan oleh masyarakat kepada pemerintah Kabupaten Padang Lawas mealui Inspektorat
            </p>
            
                        <div class="contact-us-mediasosial">
                            <h5>Media Sosial</h5>
                            <a href="https://www.instagram.com/bimbinganbareng/"><img class="ig" src="~/assets/images/ig.png" alt="not found"></a>
                            <a href="#"><img class="fb" src="~/assets/images/fb.png" alt="not found"></a>
                        </div>
                        <div class="contact-us-address">
                            <h5>Alamat</h5>
                            <p>Jl. Lintas Sibuhuan - Riau Km. 3 Sibuhuan  <br>Kabupaten Padang Lawas Provinsi Sumatera Utara</p>
                        </div>
                        <div class="contact-us-call">
                            <h5>Hubungi Kami</h5>
                            <div class="call-number">
                                <a href="https://wa.me/6282362574353?text=Selamat%20datang%20di%20Bimbinganbareng.id.%20Ada%20yang%20bisa%20kami%20bantu%3F" target="_blank"><img src="~/assets/images/call.png" alt="not found"></a>
                                <p><a href="https://wa.me/6282362574353?text=Selamat%20datang%20di%20Bimbinganbareng.id.%20Ada%20yang%20bisa%20kami%20bantu%3F" target="_blank">0823-6257-4353</a></p>
                            </div>
                        </div>
        </section>
        <section class="patent">
            <p>©Copyright 2021 Dumasinspektoratpalas.go.id</p>
        </section>
    </footer>
    
</template>

<script>
export default {

}
</script>

<style>
    .about-us {
        font-size: 18px;
        max-width: 400px;
    }
    .contact-us{
        text-align: left;
    }
    .about-us-title h5 {
        font-size: 20px;
        font-weight: 700;
    }
    .contact-us-address p{
        font-size: 16px;
    }
    .about-us p{
        font-size: 16px;
    }
    .contact-us-mediasosial h5 {
        font-weight: bold;
    }
    .ig {
        object-fit: cover;
    }
    .fb {
        object-fit: contain;
    }
    .contact-us-address h5{
        margin-top: 20px;
        font-weight: bold;
    }
    .contact-us-call h5 {
        font-weight: bold;
        margin-top: 20px;
    }
    .call-number img {
        margin-right: 20px;
        object-fit: cover;
    }
    .call-number {
        font-weight: 700;
        margin-top: 15px;
        display: flex;
        justify-content: left;
        align-items: flex-end;
    }
   
    
    /* .about-us .about-us-title h4::after {
        content: '_____';
        display: block;
        color: #4abeed;
        font-size: 30px;
        margin: -10px 0px 15px 0px;
    }
    .contact-us .contact-us-title h4::after{
        content: '_____';
        display: block;
        color: #4abeed;
        font-size: 30px;
        margin: -10px 0px 15px 0px;
    }
    .email-us .email-us-title h4::after{
        content: '_____';
        display: block;
        color: #4abeed;
        font-size: 30px;
        margin: -10px 0px 15px 0px;
    } */
    /* .phone{
        list-style-type: none;
        
    } */
    .patent{
        /* border-top: 1px solid #bbb; */
        background-color:#E2E2E2;
        text-align: left;
    }
    .patent p{
        font-size: 16px;
        font-weight: 700;
        padding: 15px;
        margin-left: 100px;
        color: #0B090A;
        margin-bottom: 0px;
    }
    @media(max-width: 578px) {
        .contact-us, .email-us{
            margin-top: 30px;
        }
        .patent p {
            width: 100%;
            margin: 0px 0px;
            padding-left: 30px;
            font-size: 12px;
        }
        .row {
            padding: 0px 20px;
        }
    }
</style>

