<template>
    <div class="running">
        <marquee class="running-text" direction="left">SELAMAT DATANG DI SITUS RESMI PELAYANAN PENGADUAN MASYARAKAT E-DUMAS INSPEKTORAT PEMKAB PADANG LAWAS</marquee>
    </div>
</template>

<script>
export default {

}
</script>

<style>
    .running {
        margin: 60px 0px 0px 0px;
        background-color: rgba(46, 44, 44, 0.7);
        height: 20px;
    }
    .running-text {
        color: white;
        font-weight: 700;
        font-size: 13px;
        margin-top: 2px;
    }
     @media (max-width: 792px) {
         .running {
             height: 15px;
         }
         .running-text {
             font-size: 7px;
             margin-bottom: 3px;
         }
     }
</style>