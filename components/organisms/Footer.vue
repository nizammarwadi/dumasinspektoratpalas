<template>
    <footer>
        <section id="footer" class="footer">
            <div class="title">
                <div>
                    <h5>E-DUMAS INSPEKTORAT PALAS</h5>
                </div>
                <p>E-Dumas Inspektorat Palas adalah Proses Penyampaian Informasi yang berisi keluhan dan ketidakpuasan 
                    yang disampaikan oleh masyarakat kepada pemerintah Kabupaten Padang Lawas mealui Inspektorat
                </p>
            </div>
            <div class="layanan">
                <h5>Jam Layanan</h5>
                <p>Senin - Jumat</p>
                <p>08.00 - 17.00</p>
        
            </div>
            <div class="contact">
                <div class="contact-us-mediasosial">
                    <h5>Media Sosial</h5>
                    <a href="https://www.instagram.com/bimbinganbareng/"><img class="ig" style="width: 50px; height: 50px" src="~/assets/images/ig.png" alt="not found"></a>
                    <a href="#"><img class="fb" style="width: 50px; height: 50px" src="~/assets/images/fb.png" alt="not found"></a>
                    <a href="#"><img class="fb" style="width: 50px; height: 50px" src="~/assets/images/yt.png" alt="not found"></a>
                </div>
                <div class="contact-us-address">
                    <h5>Alamat</h5>
                    <a href="https://www.google.co.id/maps/place/Inspektorat+Padang+Lawas/@1.0423189,99.7485166,14z/data=!4m9!1m2!2m1!1sInspektorat+Padang+Lawas!3m5!1s0x302b9bafa15eeba5:0x43a6df491960251a!8m2!3d1.0422707!4d99.7638376!15sChhJbnNwZWt0b3JhdCBQYWRhbmcgTGF3YXOSARFnb3Zlcm5tZW50X29mZmljZQ">
                    <p>Jl. Lintas Sibuhuan - Riau Km. 3 Sibuhuan  <br>Kabupaten Padang Lawas Provinsi Sumatera Utara</p></a>
                </div>
                <div class="contact-us-call">
                    <h5>Hubungi Kami</h5>
                    <div class="call-number">
                        <!-- <a href="https://wa.me/6282362574353?text=Selamat%20datang%20di%20Bimbinganbareng.id.%20Ada%20yang%20bisa%20kami%20bantu%3F" target="_blank"><img src="~/assets/images/call.png" alt="not found"></a> -->
                        <p><a href="https://wa.wizard.id/4a2aed" target="_blank">0822-5314-1167</a></p>
                        <p><a href="mailto:dumasinspektoratpls@gmail.com">dumasinspektoratpls@gmail.com</a></p>
                    </div>
                </div>
            </div>
        </section>
        <section class="patent">
            <p>©Copyright 2021 dumas-inspektorat.padanglawaskab.go.id</p>
        </section>
    </footer>
    
</template>

<script>
export default {

}
</script>

<style>
    .footer {
        color: white;
        background-image: linear-gradient(to top, rgba(0,0,0,1), rgba(0,0,0,0.4));
        padding: 70px 0px;
        display: flex;
        justify-content: space-around;
        align-items: baseline;
    }
    .footer p {
        font-weight: 200px;
    }
    .title h5 {
        font-weight: 700;
        font-size: 25px;
    }
    .title p {
        width: 500px;
        font-size: 16px;
    }
    .layanan h5 {
        font-weight: 700;
    }
    .layanan p {
        margin-bottom: 0px;
        font-weight: 400;
    }
    .contact h5 {
        font-weight: 700;
    }
    .contact p {
        font-weight: 400;
    }
    .contact-us-mediasosial img:hover {
        opacity: 0.4;
        background-color: black;
    }
    .contact-us-address {
        margin-top: 30px;
    }
    .contact-us-address p {
        color: white;
    }
    .contact-us-call {
        margin-top: 30px;
    }
    .call-number {
        display: block;
        align-items: center;
    }
    .call-number p a {
        color: white;
        margin-top: -15px;
    }
    .call-number p {
        margin-bottom: 0px;
    }
    .ig {
        object-fit: cover;
    }
    .fb {
        object-fit: contain;
    }
    .patent{
        /* border-top: 1px solid #bbb; */
        background-color:#100f0f;
        text-align: center;
    }
    .patent p{
        font-size: 12px;
        color: white;
        /* font-weight: 700; */
        padding: 15px;
        /* color: #0B090A; */
        margin-bottom: 0px;
    }
    @media(max-width: 792px) {
        .footer {
            display: block;
            width: 100%;
            /* margin: 0px 20px; */
            padding: 60px 20px;
        }
        .footer h5 {
            font-size: 16px;
        }
        .footer p {
            max-width: 100%;
            font-size: 12px;
        }
        .patent p{
            font-size: 8px;
        }
        .layanan {
            padding: 0px 0px 20px 0px;
        }
    }
</style>

