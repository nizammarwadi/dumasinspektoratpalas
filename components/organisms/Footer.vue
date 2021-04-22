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

            <div class="contact">
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
            </div>
        </section>
        <section class="patent">
            <p>©Copyright 2021 dumasinspektoratpalas.go.id</p>
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
    }
    .title h5 {
        font-weight: 700;
        font-size: 25px;
    }
    .title p {
        width: 500px;
        font-size: 16px;
    }
    .contact h5 {
        font-weight: 700;
    }
    .contact p {
        font-weight: 700;
    }
    .contact-us-address {
        margin-top: 30px;
    }
    .contact-us-call {
        margin-top: 30px;
    }
    .call-number {
        display: flex;
        align-items: center;
        /* margin-bottom: 40px; */
    }
    .call-number p {
        margin-left: 20px;
        margin-top: 20px;
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
        font-size: 16px;
        color: white;
        font-weight: 700;
        padding: 15px;
        /* color: #0B090A; */
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

