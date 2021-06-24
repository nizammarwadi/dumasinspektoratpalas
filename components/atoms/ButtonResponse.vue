<template>
    <div class="response">
        <!-- <p>Layanan Cepat</p> -->
        <div class="image">
            <a href="https://wa.wizard.id/4a2aed" target="_blank">
            <img src="~/assets/images/whatsapp.png" class="rounded-circle" alt="whatsapp"></a>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
    .response {
        position: fixed;
        right: 0;
        bottom: 0;
        display: flex;
        align-items: center;
        padding: 20px 20px;
    }
    /* .response p {
        font-weight: 700;
        color: white;
        background-color: rgb(0, 123, 255, 0.7);
        padding: 10px;
        margin: 0;
        border-radius: 5px;
    } */
    .image {
        padding: 0px 10px;
    }
    @media (max-width: 768px) {
        .response {
            padding: 10px 10px;
        }
    }

</style>