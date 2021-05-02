<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-lg-8 info-panel">
                <div class="row">
                    <div class="col-lg">
                        <a href="https://www.instagram.com/humasinspektoratpalas/">
                        <img src="~/assets/images/instagram.png" alt="instagram"></a>
                        <p>Instagram</p>
                    </div>
                    <div class="col-lg">
                        <a href="https://web.facebook.com/humasinspektoratpalas.humasinspektoratpalas/">
                        <img src="~/assets/images/facebook.png" alt="facebook"></a>
                        <p>Facebook</p>
                    </div>
                    <div class="col-lg">
                        <a href="https://wa.wizard.id/4a2aed" target="_blank">
                        <img src="~/assets/images/whatsapp.png" alt="whatsapp"></a>
                        <p>Whatsapp</p>
                    </div>
                     <div class="col-lg">
                        <a href="https://t.me/Humasinspektoratpalas" target="_blank">
                        <img src="~/assets/images/telegram.png" alt="telegram"></a>
                        <p>Telegram</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
    .info-panel {
        background-color:white;
        margin-top: -80px;
        /* padding: 20px 60px; */
        border-radius: 12px;
        box-shadow: 0 3px 20px rgba(0, 0, 0, 0.5);
        text-align: center;
    }
    .col-lg {
        padding: 30px 0px 10px 0px;
    }
    .row {
        padding: 0px 30px;
    }
    @media (max-width:792px) {
        .info-panel {
            margin-top: -60px;
        }
        .row p {
            display: none;
        }
        .col-lg {
            padding: 15px 0px 15px 0px;
        }
    }
    
</style>