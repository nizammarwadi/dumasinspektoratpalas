<template>
    <section id="about" class="about">
        <h3>SEKILAS TENTANG KAMI</h3>
        <p>Ayo lebih dekat dengan kami !!! Kami selalu berkomitmen memberikan pelayanan yang terbaik dalam fungsional pemerintahan agar tercapai kesejahteraan masyarakat yang berkeadilan sosial bagi seluruh rakyat Indonesia</p>
        <div class="content">
            <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/hEeBcrsZe04" allowfullscreen></iframe>
        </div>
    </section>
</template>

<script>
export default {
    
    }
</script>

<style>
    .about {
        margin-top: 50px;
        padding-top: 80px;
        padding-bottom: 90px;
    }
    .about h3 {
        text-align: center;
        font-weight: 700;
    }
    .about h3::after {
        content: '';
        display: block;
        border: 2px;
        width: 250px;
        background-color: #f56607;
        height: 2px;
        margin: 15px auto 30px;
    }
    .about p {
        max-width: 800px;
        text-align: center;
        margin: 0px auto;
        font-size: 20px;
    }
    .content {
        margin: 50px auto;
        text-align: center;
    }
    iframe {
        width: 800px;
        height: 400px;
        border-radius: 0px;
        /* box-shadow: 0px 0px 55px rgb(115, 125, 165); */
    }
    @media (max-width: 992px) {
        iframe {
            width: 600px;
            height: 280px;
            border-radius: 0px;
        }
        .about p {
            max-width: 100%;
            text-align: center;
            margin: 0px auto;
            font-size: 20px;
            padding: 0px 20px;
        }
    }
     @media (max-width: 592px) {
         iframe {
            width: 360px;
            height: 230px;
            border-radius: 0px;
         }
         .about P {
             font-size: 15px;
         }
         .about h3 {
             font-size: 23px;
         }
     }
</style>