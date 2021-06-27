<template>
    <div class="row mt-5 counters counters-text-dark">
        <div class="col-lg-3 col-sm-6">
            <div class="counter appear-animation animated fadeInUp appear-animation-visible" data-appear-animation="fadeInUp" data-appear-animation-delay="300">
                <i class="fa fa-user-plus"></i>
                <strong data-to="83" data-append="+">11+</strong>
                <label>Total Pengaduan</label>
                <p class="text-color-primary mb-5">Total Aduan Dilaporkan
                </p>
            </div>
        </div>
        <div class="col-lg-3 col-sm-6">
            <div class="counter appear-animation animated fadeInUp appear-animation-visible" data-appear-animation="fadeInUp" data-appear-animation-delay="600">
                <i class="fa fa-cogs"></i>
                <strong data-to="35" data-append="+">03+</strong>
                <label>Pengaduan Dalam Proses</label>
                <p class="text-color-primary mb-5">Total Aduan Dalam Proses
                </p>
            </div>
        </div>
                
				<div class="col-lg-3 col-sm-6">
					<div class="counter appear-animation animated fadeInUp appear-animation-visible" data-appear-animation="fadeInUp" data-appear-animation-delay="900">
						<i class="fa fa-clock-o"></i>
						<strong data-to="29" data-append="+">08+</strong>
						<label>Pengaduan Belum Diproses</label>
						<p class="text-color-primary mb-5">Total Aduan Belum Diproses
						</p>
					</div>
				</div>



				<div class="col-lg-3 col-sm-6">
					<div class="counter appear-animation animated fadeInUp appear-animation-visible" data-appear-animation="fadeInUp" data-appear-animation-delay="1200">
						<i class="fa fa-check-square-o"></i>
						<strong data-to="19" data-append="+">02+</strong>
						<label>Pengaduan Selesai</label>
						<p class="text-color-primary mb-5">Total Aduan Selesai
						</p>
					</div>
				</div>
			</div>
</template>

<script>
export default {

}
</script>

<style>
    .counters.counters-text-dark .counter {
        color: #2e353e !important;
    }

</style>