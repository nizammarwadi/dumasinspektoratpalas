<template>
<div class="container">
    <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="exampleModalLabel">Terima kasih, pengaduan anda akan segera kami verifikasi</h5>
                    <button type="button" @click ="$emit('click-reset')" class="close" data-dismiss="modal" aria-label="Close">
                    <span aria-hidden="true">&times;</span>
                    </button>
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
.modal-content {
    width: 350px;
    margin: 80px auto 0px;
}   
</style>