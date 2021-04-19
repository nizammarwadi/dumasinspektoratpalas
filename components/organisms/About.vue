<template>
    <section class="about">
        <h3>ABOUT SHORTLY US</h3>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Earum, dolor harum nulla debitis dolore quos sequi laboriosam beatae, quisquam aperiam magnam nostrum quasi eveniet dignissimos? Quas, odit tempora. Repudiandae, sunt.</p>
        <div class="content">
            <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/eaGm7_IoR4M" allowfullscreen></iframe>
        </div>
    </section>
</template>

<script>
export default {
    
    }
</script>

<style>
    .about {
        margin: 150px 0px;
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

</style>
<script>
export default {

}
</script>

<style>
/* .about::after {
    content: '';
    display: block;
    width: 100%;
    height: 100%;
    background-image: linear-gradient(to top, rgba(0,0,0,1), rgba(0,0,0,0.6));
    position: absolute;
    bottom: 0;       
}  */
/* .title {
    position: relative;
    z-index: 1;
} */
/* .content {
    position: relative;
    z-index: 1;
} */
/* @media(max-width: 768px) {
    .about{
        width: 100%;
        margin: 50px auto 0px;
        padding: 0px;
    }
    .about-title .content {
        width: 100%;
        margin: 0px auto;
        padding: 0px 10px 10px 10px;
        font-size: 17px;
        display: none;
                
    }
    .container .row .col{
        padding: 0px;
        margin: 0px;
        width: 100%;
        
    }
    iframe{
        width: 70%;
        height: 180px;

    } */
</style>