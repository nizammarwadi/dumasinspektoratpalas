<template>
    <section class="principle">
        <div class="principle-left">
            <div>
                <h3>Jika anda melihat penyimpangan dalam kinerja pemerintahan Kabupaten Padang Lawas, segera laporkan !!! </h3>
                <p>Partisipasi anda dalam pengaduan ini sangat berarti bagi pembangunan Kab. Padang Lawas yang BERCAHAYA (beriman, cerdas,sehat,sejahtera dan berbudaya) </p>
                <!-- <button class="btn btn-primary mr-4"> Respon Cepat</button> -->
                <button class="btn btn-danger">Span Lapor</button>

            </div>
        </div>
        <div class="principle-middle mr-2">
            <img src="~/assets/images/laptop.jpg" width="250px" height="450px" alt="not found">
        </div>
          <div class="principle-right">
            <img src="~/assets/images/dpr.jpg" width="200px" height="330px" alt="not found">
        </div>
    </section>
</template>

<script>
export default {

}
</script>

<style>
    .principle {
        display: flex;
        align-items: center;
        justify-content: center;
        margin-bottom: 150px;
    }
    .principle-left {
        max-width: 550px;
        background-color: rgb(245, 246, 247);
        padding: 20px 20px;
        position: relative;
        margin-right: -40px;
        box-shadow: 10px 10px 5px white;
        opacity: .9;
    }
    .principle-left h3 {
        font-weight: 700;
    }
    .principle-middle img {
        object-fit: cover;
        /* opacity: .9; */
    }
    .principle-right img {
        object-fit: cover;
    }
    @media (max-width: 792px) {
        .principle {
            padding: 0px 20px;
        }
        .principle-left {
            max-width: 30%;
            background-color: rgb(245, 246, 247);
            padding: 20px 0px;
            position: relative;
            margin-right: -35px;
            box-shadow: 10px 10px 5px white;
            opacity: .9;
        }
        .principle-left h3 {
            font-weight: 700;
            font-size: 14px;
        }
        .principle-left p {
            font-size: 10px;
        }
        .principle-middle img {
            width: 130px;
            height: 300px;
        }
        .principle-right img {
            width: 75px;
            height: 190px;
        }
    }

</style>