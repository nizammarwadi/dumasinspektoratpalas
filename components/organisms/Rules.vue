<template>
    <section class="rules">
        <div class="rulesTop">
            <div class="container">
                <div class="rulesTopLine row">
                    <div class="rulesContent col">
                        <h3>LATAR BELAKANG</h3>
                        <div class="list-group">
                            <a href="#" class="list-group-item list-group-item-action list-group-item-primary">Terbatasnya komunikasi pemerintah dengan warga</a>
                            <a href="#" class="list-group-item list-group-item-action list-group-item-secondary">Penyampaian aspirasi masyarakat tidak mudah</a>
                            <a href="#" class="list-group-item list-group-item-action list-group-item-success">Pengaduan yang disampaiakan tidak bisa dimonitor tindak lanjutnya</a>
                            <a href="#" class="list-group-item list-group-item-action list-group-item-danger">Kurangnya fasilitas untuk partisipasi masyarakat dalam pengaduan</a>
                            <a href="#" class="list-group-item list-group-item-action list-group-item-warning">Inovasi dibidang teknologi dalam instansi pemerintah </a>
                        </div>
                    </div>
                    <div class="col">
                        <h3>MAKSUD</h3>
                        <div class="list-group">
                            <a href="#" class="list-group-item list-group-item-action list-group-item-light">Hadirnya E-dumas Inspektorat Pemkab Padang Lawas untuk memudahkan masyarakat dalam menyampaikan pengaduan ataupun tindak kecurangan diwilayah pemerintah Padang Lawas secara online
                            </a>
                        </div>
                    </div>
                </div>
            </div>
             <div class="container">
                <div class="rulesTopLine row">
                    <div class="rulesContent col">
                        <h3>TUJUAN</h3>
                        <div class="list-group">
                            <a href="#" class="list-group-item list-group-item-action list-group-item-light">E-dumas bertujuan meningkatkan kualitas komunikasi pemerintah daerah dengan masyarakat dalam pelaksaan pembangunan Pemerintah Padang Lawas yang BERCAHAYA (beriman, cerdas, sehat, sejahtera dan berbudaya)
                            </a>
                        </div>
                    </div>
                    <div class="col">
                        <h3>MANFAAT</h3>
                        <div class="list-group">
                            <a href="#" class="list-group-item list-group-item-action list-group-item-primary">Lancarnya komunikasi masyarakat dengan pemerintah</a>
                            <a href="#" class="list-group-item list-group-item-action list-group-item-secondary">Partisipasi masyarakat dalam pembangunan pemerintah daerah yang bersih</a>
                            <a href="#" class="list-group-item list-group-item-action list-group-item-success">Transparansi penanganan pengaduan dari masyarakat</a>
                            <a href="#" class="list-group-item list-group-item-action list-group-item-danger">Pemerintah dapat memonitoring pengaduan masyarakat dalam instansi pemerintah daerah</a>
                            <a href="#" class="list-group-item list-group-item-action list-group-item-warning">Terukurnya kinerja SKPD dalam menangani pengaduan masyarakat</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {

}
</script>

<style>
    .list-group a {
        text-align: left;
    }
    .rules {
        margin-bottom: 140px;
    }
    .rulesTopLine {
        margin-bottom: 80px;
    }
    .rulesTopLine h3 {
        font-size: 28px;
        font-weight: 700;
    }
     .rulesTopLine h3::after {
        content: '';
        display: block;
        border: 2px;
        width: 100px;
        background-color: #f56607;
        height: 2px;
        margin: 15px auto 30px;
    }
    @media (max-width: 768px) {
        .rulesTopLine {
            display: block;
        }
        .rulesContent {
            margin-bottom: 30px;
        }
    }

</style>